# Broadcast - Decentralized Community Messaging Platform

> **A hackathon project** - A modern, decentralized messaging and communication platform built for communities, featuring XMTP integration, AI agents, and comprehensive Web3 features.

## 🎯 Project Overview

Broadcast is a comprehensive decentralized messaging platform designed to replace traditional community communication tools like WhatsApp and Telegram. Built with modern Web3 technologies, it provides secure, encrypted messaging, AI-powered agents, and seamless blockchain integration.

### Why Broadcast?

- **Decentralized & Secure**: End-to-end encrypted messaging using XMTP protocol
- **Community-Focused**: Designed specifically for communities that currently rely on WhatsApp
- **AI-Powered**: Intelligent agents for community management and automation
- **Web3 Native**: Built with blockchain features for modern communities
- **Multi-Platform**: Web and mobile applications with consistent experience
- **Open Source**: Fully open-source and hackable for developers

## 🏗️ Architecture

Broadcast consists of three main components:

```
broadcast-build/
├── broadcast-web/          # Next.js web application
├── broadcast/              # React Native mobile app
└── broadcast-agents/       # AI agents backend service
```

## 🚀 Features

### 💬 Decentralized Messaging
- **XMTP Integration**: End-to-end encrypted group chats using XMTP protocol
- **Wallet-based Authentication**: Connect with any Ethereum wallet for secure identity
- **Real-time Messaging**: Live updates and instant message delivery
- **Group Chat Management**: Create, join, and manage group conversations
- **Multi-chain Support**: Ethereum, Polygon, Mumbai, and Sepolia networks

### 🤖 AI Agents System
- **Multi-Agent Management**: Create, start, stop, and monitor multiple AI agents
- **Agent Marketplace**: Browse and use community-created agents
- **Automated Responses**: Set up automated responses and actions
- **Blockchain Operations**: Wallet management and blockchain interactions via AgentKit
- **Health Monitoring**: Automatic health checks and agent recovery

### 🎨 Advanced UI/UX
- **Modern Design**: Clean, modern interface with consistent theming
- **Theme System**: Light/dark mode with comprehensive color palettes
- **Responsive Design**: Mobile-first approach with adaptive layouts
- **WhatsApp-inspired Interface**: Familiar messaging experience
- **Pull-to-Refresh**: Update content with intuitive gestures

### 🔐 Security & Privacy
- **End-to-End Encryption**: All messages encrypted using XMTP's MLS protocol
- **Decentralized Storage**: No central server controls your conversations
- **Wallet Authentication**: Secure identity verification
- **Privacy-First**: User consent controls and data ownership

### 📱 Multi-Platform Support
- **Web Application**: Next.js 15 with App Router and TypeScript
- **Mobile Application**: React Native with native performance
- **Cross-Platform**: Consistent experience across web and mobile
- **Deep Linking**: Seamless wallet connections and navigation

## 🛠️ Tech Stack

### Web Application (`broadcast-web/`)
- **Framework**: Next.js 15 with App Router
- **Language**: TypeScript
- **Styling**: Tailwind CSS 4
- **UI Components**: Radix UI + Custom Components
- **Messaging**: XMTP Protocol
- **Blockchain**: Ethers.js + Viem + Wagmi
- **State Management**: TanStack Query + React Context
- **Theming**: next-themes + Custom Theme System

### Mobile Application (`broadcast/`)
- **Framework**: React Native 0.79.3
- **Language**: TypeScript 5.0.4
- **State Management**: Redux Toolkit 2.8.2
- **Navigation**: React Navigation 7.x
- **Wallet Integration**: MetaMask SDK + WalletConnect
- **Messaging**: XMTP React Native SDK
- **Blockchain**: Ethers.js 6.14.3

### AI Agents Service (`broadcast-agents/`)
- **Runtime**: Node.js 20+
- **Framework**: Express.js 5.1.0
- **Language**: TypeScript 5.8.3
- **AI Framework**: LangChain + OpenAI
- **Blockchain**: Coinbase AgentKit
- **Messaging**: XMTP Node SDK
- **Storage**: File-based persistent storage

## 📦 Quick Start

### Prerequisites
- Node.js >= 20
- React Native CLI (for mobile development)
- iOS: Xcode (for iOS development)
- Android: Android Studio (for Android development)

### 1. Clone the Repository
```bash
git clone <repository-url>
cd broadcast-build
```

### 2. Web Application Setup
```bash
cd broadcast-web
npm install
npm run dev
```
Navigate to [http://localhost:3000](http://localhost:3000)

### 3. Mobile Application Setup
```bash
cd broadcast
npm install
# iOS (macOS only)
cd ios && pod install && cd ..
# Start Metro bundler
npm start
# Run on device/simulator
npm run ios     # or npm run android
```

### 4. AI Agents Service Setup
```bash
cd broadcast-agents
npm install
# Create .env file with required variables
cp .env.example .env
# Edit .env with your credentials
npm run dev
```

## 🔧 Configuration

### Environment Variables

#### Web Application
Create `broadcast-web/.env.local`:
```env
NEXT_PUBLIC_XMTP_ENVIRONMENT=dev
NEXT_PUBLIC_ALCHEMY_API_KEY=your_alchemy_key
NEXT_PUBLIC_INFURA_API_KEY=your_infura_key
```

#### Mobile Application
Create `broadcast/.env`:
```env
WALLETCONNECT_PROJECT_ID=your_project_id
METAMASK_DEEP_LINK=your_deep_link_scheme
```

#### AI Agents Service
Create `broadcast-agents/.env`:
```env
WALLET_KEY=your_private_key_here
ENCRYPTION_KEY=your_encryption_key_here
XMTP_ENV=dev
CDP_API_KEY_ID=your_cdp_api_key_id
CDP_API_KEY_SECRET=your_cdp_api_key_secret
NETWORK_ID=your_network_id
OPEN_AI_KEY=your_openai_api_key
```

## 📱 Usage Guide

### Connecting Your Wallet
1. Click the wallet icon in the application
2. Connect your Ethereum wallet (MetaMask recommended)
3. Approve the XMTP authentication signature

### Creating Group Chats
1. Ensure your wallet is connected
2. Click the "+" button in the chat sidebar
3. Fill in group details:
   - Group Name (required)
   - Description (optional)
   - Group Image URL (optional)
   - Member Addresses (Ethereum addresses separated by commas)
4. Click "Create Group"

### Using AI Agents
1. Navigate to the Agents tab
2. Browse available agents or create your own
3. Start an agent and interact with it via chat
4. Monitor agent health and performance

### Theme Customization
- Use the theme toggle in the header
- Choose from Light, Dark, or System themes
- Visit `/theme-demo` for a comprehensive theme showcase

## 🏗️ Project Structure

### Web Application
```
broadcast-web/src/
├── app/                    # Next.js App Router
│   ├── layout.tsx         # Root layout with theme provider
│   ├── page.tsx           # Main application page
│   ├── globals.css        # Global styles and theme variables
│   └── theme-demo/        # Theme demonstration page
├── components/            # React components
│   ├── ui/               # Reusable UI components
│   ├── screens/          # Main application screens
│   ├── modals/           # Modal components
│   └── App/              # Core application components
├── contexts/             # React contexts
│   └── XMTPContext.tsx   # XMTP state management
├── hooks/                # Custom React hooks
├── lib/                  # Utility libraries
└── data/                 # Static data and constants
```

### Mobile Application
```
broadcast/src/
├── components/     # Reusable UI components
│   └── wallet/    # Wallet-related components
├── screens/        # Screen components
│   ├── ChatsScreen.tsx
│   ├── StatusScreen.tsx
│   ├── CalendarScreen.tsx
│   ├── WalletsScreen.tsx
│   ├── AgentsScreen.tsx
│   └── ...        # Other screens
├── navigation/     # Navigation configuration
├── store/          # Redux store and slices
├── types/          # TypeScript type definitions
├── hooks/          # Custom React hooks
├── services/       # API and service functions
├── config/         # App configuration
└── constants/      # App constants and theme
```

### AI Agents Service
```
broadcast-agents/src/
├── types/           # TypeScript type definitions
├── utils/           # Utility functions and helpers
│   ├── config.ts    # Configuration management
│   ├── errors.ts    # Error handling and custom errors
│   ├── logger.ts    # Centralized logging
│   └── storage.ts   # File storage operations
├── broadcast.agent.ts           # Main agent service
├── broadcast.agent.manager.ts   # Agent lifecycle management
├── helper.ts        # XMTP and agent initialization
├── index.ts         # Express server and API routes
├── prompt.ts        # Agent prompt templates
└── xmtp.ts          # XMTP utilities
```

## 🚀 Available Scripts

### Web Application
```bash
npm run dev          # Start development server
npm run dev:turbo    # Start with Turbopack for faster builds
npm run build        # Build for production
npm run start        # Start production server
npm run lint         # Run ESLint
```

### Mobile Application
```bash
npm start            # Start Metro bundler
npm run ios          # Run on iOS simulator
npm run android      # Run on Android emulator
npm test             # Run tests
npm run lint         # Lint code
```

### AI Agents Service
```bash
npm run dev          # Start development server with hot reload
npm run build        # Build TypeScript to JavaScript
npm start            # Start production server
npm run lint         # Run ESLint
npm run format       # Format code with Prettier
npm run gen:keys     # Generate encryption keys
```

## 🔐 Security Features

- **End-to-End Encryption**: XMTP's MLS protocol for message security
- **Forward Secrecy**: Past messages remain secure even if keys are compromised
- **Post-Compromise Security**: New keys are generated after compromise
- **Input Validation**: All inputs validated using Zod schemas
- **CORS Protection**: Configurable CORS settings
- **Security Headers**: Helmet.js for security headers
- **Rate Limiting**: Built-in protection against abuse

## 📊 Monitoring & Logging

### Logging Levels
- `error` - Critical errors that need immediate attention
- `warn` - Warning conditions
- `info` - General information
- `debug` - Detailed debugging information

### Health Checks
- Agent health monitoring with automatic restart
- Storage directory monitoring
- Memory usage tracking
- XMTP connection status

## 🧪 Testing

```bash
# Web Application
cd broadcast-web
npm test

# Mobile Application
cd broadcast
npm test

# AI Agents Service
cd broadcast-agents
npm test
```

## 🚀 Deployment

### Web Application
```bash
cd broadcast-web
npm run build
npm start
```

### Mobile Application
- **iOS**: Build and deploy through Xcode
- **Android**: Build APK/AAB through Android Studio

### AI Agents Service
```bash
cd broadcast-agents
npm run build
npm start
```

### Docker Deployment
```dockerfile
FROM node:20-alpine
WORKDIR /app
COPY package*.json ./
RUN npm ci --only=production
COPY dist ./dist
EXPOSE 5000
CMD ["node", "dist/index.js"]
```

## 📚 Documentation

- [XMTP Integration Guide](broadcast-web/XMTP_INTEGRATION.md)
- [XMTP Troubleshooting](broadcast-web/XMTP_TROUBLESHOOTING.md)
- [Theme System Documentation](broadcast-web/THEME_SYSTEM.md)
- [MetaMask Setup Guide](broadcast/METAMASK_SETUP.md)
- [WalletConnect Setup Guide](broadcast/WALLETCONNECT_SETUP.md)
- [Deep Linking Setup Guide](broadcast/DEEP_LINKING_SETUP.md)
- [Troubleshooting Guide](broadcast/TROUBLESHOOTING_CRASH.md)

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🔗 Resources

- [XMTP Documentation](https://docs.xmtp.org/)
- [Next.js Documentation](https://nextjs.org/docs)
- [React Native Documentation](https://reactnative.dev/)
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [Radix UI Documentation](https://www.radix-ui.com/)
- [Ethereum Documentation](https://ethereum.org/developers/)
- [Coinbase AgentKit](https://docs.coinbase.com/agentkit/docs)

## 🆘 Support

If you encounter any issues:

1. Check the troubleshooting guides in each component
2. Review browser/device console for error messages
3. Ensure your wallet is properly connected
4. Verify environment configuration

For additional support, please open an issue on GitHub.

## 🏆 Hackathon Project

This project was built for a hackathon and demonstrates:
- Modern Web3 development practices
- Cross-platform application development
- AI integration with blockchain
- Decentralized messaging protocols
- Comprehensive security implementation

---

**Built with ❤️ for the Web3 community**


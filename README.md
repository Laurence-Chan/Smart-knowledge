# Smart Knowledge

**English | [中文](./README.md)**

Smart Knowledge is an AI-enhanced knowledge management plugin designed for Obsidian that makes your personal knowledge base smarter and more efficient through semantic understanding and intelligent recommendation technologies.

## ✨ Core Features

### 🔍 Semantic Search
- **Natural Language Retrieval**: No more relying on keyword matching - describe what you're looking for in natural language
- **Vector Indexing**: Built on advanced embedding models to create semantic vector indexes for all your notes
- **Quick Access**: Fast access through command palette or toolbar to open semantic search modal

### 🤖 AI-Powered Q&A
- **RAG Q&A System**: Combines Retrieval-Augmented Generation technology to answer questions based on your notes
- **@ Mention Feature**: Use `@note-title` to directly reference specific notes in conversations
- **Sidebar View**: Independent AI assistant panel supporting continuous conversations
- **Context Awareness**: Automatically combines current active notes and related content to provide answers

<img width="1119" height="1027" alt="截屏2025-09-23 下午9 10 23" src="https://github.com/user-attachments/assets/638e47ef-616c-4a29-93cc-495ba1da00fd" />

### 📚 Intelligent Recommendations
- **Real-time Associations**: Automatically recommends related documents based on currently reading note content
- **Similarity Scoring**: Shows relevance degree of recommended notes to help judge association strength
- **Relationship Explanations**: Optional generation of recommendation reasons to understand the logic behind note associations
- **Sidebar Integration**: Continuously displayed in right sidebar without interfering with normal note browsing

<img width="1119" height="670" alt="截屏2025-09-23 下午9 05 43" src="https://github.com/user-attachments/assets/826b869e-1b94-4985-8506-06f5bc3f74b7" />

### 🎯 Multi-Model Support
- **Flexible Configuration**: Supports mainstream AI services like OpenAI, Claude, Deepseek, Qwen, etc.
- **Proxy Services**: Built-in common proxy service presets with support for custom API endpoints
- **Service Fallback**: Multi-service automatic switching ensures functionality stability

## 🚀 Quick Start

### Installation Methods

#### Method 1: Manual Installation (Recommended)
1. Download the latest version from [Releases](https://github.com/laurence-chan/smart-knowledge/releases)
2. Extract files to `[your-vault]/.obsidian/plugins/smart-knowledge/` directory
3. Enable "Smart Knowledge" plugin in Obsidian settings

#### Method 2: Developer Installation
```bash
# Clone code to plugin directory
git clone https://github.com/laurence-chan/smart-knowledge.git
cd smart-knowledge
npm install
npm run build

# Copy build files to Obsidian plugin directory
cp main.js manifest.json styles.css /path/to/your/vault/.obsidian/plugins/smart-knowledge/
```

### Basic Configuration

1. **Open Plugin Settings**
   - Go to Obsidian Settings → Smart Knowledge

2. **Configure Embedding Service** (Required)
   - Select embedding model provider 
   - Enter corresponding API key

3. **Configure Chat Service** (Optional)
   - Select chat model provider
   - Enter corresponding API key

4. **Initialize Knowledge Base**
   - Use command palette search: "Smart Knowledge: Initialize Knowledge Base Index"
   - Wait for indexing completion (status bar will show progress)

## 🎮 Usage Guide

### Command Palette Functions
- `Smart Knowledge: Initialize Knowledge Base Index` - Generate vector indexes for all notes
- `Smart Knowledge: Smart Search Notes` - Open semantic search modal
- `Smart Knowledge: Open AI Chat Panel` - Open AI Q&A view in sidebar
- `Smart Knowledge: View Knowledge Base Status` - Check index status and service configuration
- `Smart Knowledge: Rebuild Knowledge Base Index` - Clear and rebuild all vector indexes

### Interface Elements

#### Status Bar Indicator
- 🧠 `number` - Shows number of indexed vectors, click to view detailed status
- ⚠️ Warning icon - Indicates need for API configuration or re-indexing

#### Sidebar Views
- **Recommendation View**: Automatically shows related recommendations based on current note
- **AI Chat View**: Continuous AI assistant conversation interface

#### Search Features
- Enter natural language descriptions in search box
- Supports fuzzy matching and semantic understanding
- Shows similarity scores and preview content

## ⚙️ Advanced Configuration

### Proxy Service Settings
Plugin includes multiple proxy service presets:
- **API2D**: China-friendly proxy service
- **CloseAI**: High-stability proxy service
- **AI Town**: Multi-model support proxy platform
- **Custom**: Configure your own proxy endpoints

### Performance Optimization
- **Recommendation Count**: Control number of recommended notes displayed each time (default 5)
- **Similarity Threshold**: Set minimum similarity requirement for recommendations (default 0.4)
- **Enhanced Search**: Enable smart caching and result optimization (recommended enabled)

### File Processing
- **Auto Sync**: Automatically update vector indexes after file modifications
- **Smart Chunking**: Long documents automatically split to ensure embedding quality
- **Format Support**: Full support for Markdown syntax and metadata

## 🔒 Privacy and Security

- **Local Storage**: All API keys stored only in local vault
- **Data Processing**: Vector data cached locally to reduce duplicate API calls
- **Encryption Protection**: Sensitive configuration information encrypted storage
- **Network Security**: Supports custom proxies to ensure secure data transmission

## 📊 System Requirements

- **Obsidian Version**: 0.15.0 or higher
- **Network Connection**: Requires access to configured AI service APIs
- **Storage Space**: Vector index files occupy minimal disk space
- **Memory Usage**: Dynamically adjusts based on vault size, typically uses minimal memory

## 🔧 Troubleshooting

### Common Issues

**Q: Status bar shows "API Configuration Required"**
A: Check if API keys in plugin settings are correctly filled, save settings and restart plugin.

**Q: Search results inaccurate or no results**
A: Confirm knowledge base indexing is complete, try rebuilding index or adjusting similarity threshold.

**Q: API call failures or timeouts**
A: Check network connection and API keys, consider using proxy services or switching service providers.

**Q: Vector dimension mismatch error**
A: Indicates embedding model was changed, need to execute "Rebuild Knowledge Base Index" to regenerate vectors.

### Debug Information
- Enable Obsidian developer tools to view console logs
- View detailed service status information in plugin settings
- Use "View Knowledge Base Status" command to check system health

## 🤝 Contributing

Issues and Pull Requests are welcome!

### Development Environment Setup
```bash
git clone https://github.com/laurence-chan/smart-knowledge.git
cd smart-knowledge
npm install
npm run dev  # Start development mode
```

### Build and Testing
```bash
npm run build     # Production build
npm run version   # Version management
```

## 📄 License

This project is licensed under the [MIT](./LICENSE) license.

---

**Make your knowledge base smarter, make knowledge discovery more efficient!** 🧠✨

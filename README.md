# PromptMooi

**PromptMooi** is a mobile-first web app that transforms messy developer input—informal text, code snippets, logs, and small extracts—into clean, structured prompts tailored for different coding AIs and IDEs like Cursor, Claude, and ChatGPT. Write once, generate prompts for many tools.

## Features

- **Mobile-first design**: Comfortable input areas and touch-friendly buttons optimized for any screen size
- **Multi-tool support**: Generate prompts customized for Cursor, Claude, ChatGPT, and more
- **Smart input normalization**: Automatically cleans up messy input while preserving code and structure
- **Task detection**: Automatically identifies task types (bugfix, refactor, feature, tests, docs) to add context
- **Extensible architecture**: Modular adapters and core logic make it easy to add new tools or refine prompt generation
- **Capacitor-ready**: Clean, modular React structure prepared for iOS/Android wrapping with Capacitor

## Getting Started

### Prerequisites

- Node.js 16+ and npm

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/saritadf/prompt-mooi.git
   cd prompt-mooi
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Start the development server:
   ```bash
   npm run dev
   ```

   The app will open at `http://localhost:5173/` in your browser.

### Build for Production

```bash
npm run build
```

This creates an optimized production build in the `dist/` directory.

## Project Structure

```
prompt-mooi/
├── public/               # Static assets (index.html, favicon)
├── src/
│   ├── main.tsx         # App entry point
│   ├── ui/              # React components and pages
│   │   └── App.tsx
│   ├── styles/          # Global and responsive CSS (mobile-first)
│   │   └── main.css
│   ├── core/            # Core logic for normalization, detection, and prompt building
│   │   ├── normalizeInput.ts
│   │   ├── detectTaskType.ts
│   │   └── buildPrompt.ts
│   └── adapters/        # Per-tool prompt generators
│       ├── cursorAdapter.ts
│       ├── claudeAdapter.ts
│       └── chatgptAdapter.ts
├── package.json
├── vite.config.ts
├── tsconfig.json
└── README.md
```

## Tech Stack

- **React 18** with TypeScript for type-safe, modern UI
- **Vite** for fast development and optimized production builds
- **CSS3** with mobile-first responsive design
- **Modular architecture** ready for Capacitor mobile wrapping

## Roadmap

- [ ] Enhanced task type detection with AI/ML
- [ ] Additional target tools (VS Code, JetBrains IDEs)
- [ ] Prompt templates and customization UI
- [ ] User preferences (syntax highlighting, theme, etc.)
- [ ] Integration with clipboard and file upload
- [ ] iOS/Android app via Capacitor
- [ ] API backend for advanced prompt refinement

## Contributing

Contributions are welcome! Feel free to open issues or submit pull requests.

## License

MIT
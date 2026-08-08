<p align="center">
  <a href="https://coreui.com">
    <img src="./icon.svg" height="96">
    <h3 align="center">CoreUI Design System</h3>
  </a>
  <p align="center">The Design System You Need</p>
</p>

[Join the CoreUI Community](https://discord.gg/coreui)

## Introduction

A CLI for adding CoreUI's Tailwind CSS v4.1 styles to your project with CSS-first configuration.

## Usage

Use the `tailwind` command to initialize Tailwind CSS v4.1 with CoreUI design system for your project.

> [!CAUTION]
> This will overwrite your CSS and `tailwind.config` files with Tailwind v4.1 CSS-first configuration.

```bash
npx @coreui/cli tailwind
```

This command will:

- Detect if you're using TypeScript
- Install Tailwind CSS v4.1 packages (`tailwindcss@next`, `@tailwindcss/postcss@next`)
- Ask for your preferred primary color (Blue, Purple, Orange, Sky)
- Ask for your preferred neutral color (Gray, Slate)
- Ask for your preferred color format (OKLCH recommended, HEX, RGB, HSL)
- Prompt you to choose a prefix for CoreUI's classes if needed
- Generate CSS-first configuration with `@theme` directive
- Set up all CoreUI design tokens and colors

> [!NOTE]  
> A CSS file with Tailwind directives and a `tailwind.config` file must exist in your project.

## What's New in v0.0.6

- 🐛 **Bug Fixes**: Fixed typography [object Object] rendering issues
- 🔧 **Complete Typography System**: All typography properties (fontSize, lineHeight, letterSpacing, fontWeight) now properly exported
- 🔄 **Backward Compatibility**: Legacy TypeScript exports available for v0.0.2 migration
- ✨ **Enhanced Shadow System**: Fixed theme() references for Tailwind v4.1 compatibility

## What's New in v0.0.3

- ✨ **Tailwind CSS v4.1 Support**: Full compatibility with the latest Tailwind CSS
- 🎨 **CSS-First Configuration**: Uses `@theme` directive instead of JavaScript config
- 🌈 **OKLCH Color System**: Modern color space for more vivid colors (default)
- ⚡ **Simplified Setup**: Streamlined installation process
- 🔧 **Modern CSS Features**: Support for cascade layers and advanced CSS properties

## Migration from v0.0.2

If you're migrating from v0.0.2, you can still use TypeScript exports for backward compatibility:

```typescript
// For backward compatibility
import { texts, shadows, borderRadii } from '@coreui/cli/legacy-exports';
```

However, we recommend using the new CSS-first approach with `@theme` variables for better performance and Tailwind v4.1 compatibility.

## License

[MIT](./LICENSE)

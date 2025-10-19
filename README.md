# GOLRR

> Lightweight terminal theming package for Go CLI apps

Golrr provides a simple, expressive way to manage colors, styles, and themes in Go CLI environments. It helps to build consistent, colorful, and human-friendly command-line interfaces with minimal dependencies.

### ✨ Features

- TrueColor (RGB / HEX) and ANSI-256 color support  
- Chainable, composable style definitions  
- Cross-platform with `TTY` and `NO_COLOR` detection  
- Reusable theme presets (Catppuccin, Gruvbox, Dracula, and more)

### 🚀 Installation

```sh
go get github.com/patpuccin/golrr
```

### 📖 Usage

#### Basic usage

```go
package main

import (
	"fmt"
	"github.com/patpuccin/golrr"
)

func main() {
	theme := golrr.CatppuccinMocha
	style := golrr.NewStyle().FG(theme.Primary).Bold().Underline()
	fmt.Println(style.Sprint("Hello, Golrr!"))
}
```

#### Custom themes

```go
package main

import (
	"fmt"
	"github.com/patpuccin/golrr"
)

func main() {
    myTheme := golrr.Theme{
        Background:    golrr.ColorFromHex("#1e1e2e"),
        BackgroundAlt: golrr.ColorFromHex("#181825"),
        Foreground:    golrr.ColorFromHex("#cdd6f4"),
        ForegroundAlt: golrr.ColorFromHex("#bac2de"),
        Primary:       golrr.ColorFromHex("#cba6f7"),
        Secondary:     golrr.ColorFromHex("#f2cdcd"),
        Accent:        golrr.ColorFromHex("#fab387"),
        Highlight:     golrr.ColorFromHex("#f5e0dc"),
        Muted:         golrr.ColorFromHex("#6c7086"),
        Red:           golrr.ColorFromHex("#f38ba8"),
        Green:         golrr.ColorFromHex("#a6e3a1"),
        Yellow:        golrr.ColorFromHex("#f9e2af"),
        Blue:          golrr.ColorFromHex("#89b4fa"),
        Purple:        golrr.ColorFromHex("#cba6f7"),
        Orange:        golrr.ColorFromHex("#fab387"),
    }
    style := golrr.NewStyle().FG(myTheme.Primary).Bold().Underline()
    fmt.Println(style.Sprint("Hello, Golrr!"))
}
```

### 🧱 Projects using Golrr

- [Asky](https://github.com/patpuccin/asky) – Simple interactive prompt library for Go

### 🪪 License

[MIT License](/LICENSE) - © 2025 Patrick Ambrose
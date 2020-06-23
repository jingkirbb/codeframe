## Codeframe

![Rust CI](https://github.com/TheWebDevel/codeframe/workflows/Rust%20CI/badge.svg)

Capture pretty codeframes from a code snippet.

```rust
use codeframe::Codeframe;

let raw_lines = "macro_rules! test_simple_style {
    ($string:expr, $style:ident) => {
        #[test]
        fn $style() {
            assert_eq!(
                s.$style().to_string(),
                ansi_term::Style::new().$style().paint(s).to_string()
            )
        }
    };
}";
let codeframe = Codeframe::new(raw_lines, 5).set_color("red").capture();
```

![Imgur](https://i.imgur.com/vJzKeCr.png)

### Colors Supported

- Black
- Red
- Green
- Yellow
- Blue
- Magenta or (Purple)
- Cyan
- White

### Features

- [x] line
- [x] raw lines
- [x] color
- [ ] file path
- [ ] codeframe!() or codeframe!("red") Macro
- [ ] with column (Highlight Column)
- [ ] with line_above
- [ ] with line_below

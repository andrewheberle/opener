# opener

A Go package that opens URLs in the user’s default browser, with support for Windows, macOS, Linux, and WSL.

## Installation

```sh
go get github.com/andrewheberle/opener
```

## Usage

```go
import "github.com/andrewheberle/opener"

err := opener.OpenUrl("https://example.com")
if err != nil {
    log.Fatal(err)
}
```

## Platform Support

| Platform                   | Method         |
|----------------------------|----------------|
| Windows                    | `cmd /c start` |
| macOS                      | `open`         |
| Linux                      | `xdg-open`     |
| WSL                        | `cmd /c start` |
| FreeBSD / OpenBSD / NetBSD | `xdg-open`     |

## API

### `OpenUrl(url string) error`

Opens the specified URL in the user’s default browser. Returns an error if the
underlying command cannot be started.

## License

MIT

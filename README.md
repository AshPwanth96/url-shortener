# url-shortener
Developed a Go URL shortener using `github.com/go-chi/chi/v5` for routing and `github.com/lithammer/shortuuid/v4` for short URL generation. Handles concurrent access with `sync.Mutex`, featuring endpoints for creating (`POST /short-it`) and redirecting (`GET /short/{key}`) URLs. Implements logging and error handling for reliability.

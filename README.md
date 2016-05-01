# Bamboo.SMTPAdapter

An Adapter for the [Bamboo](https://github.com/thoughtbot/bamboo) email app.

## Installation

The package can be installed as:

1. Add `bamboo_smtp` to your list of dependencies in `mix.exs`:

  ```elixir
  def deps do
    [{:bamboo_smtp, "~> 0.0.1"}]
  end
  ```

2. Add `bamboo` to your list of applications in `mix.exs`:

  ```elixir
  def application do
    [applications: [:bamboo]]
  end
  ```

3. Setup your SMTP configuration:

  ```elixir
  # In your config/config.exs file
  config :my_app, MyApp.Mailer,
    adapter: Bamboo.SMTPAdapter,
    server: "smtp.domain",
    port: 1025,
    username: "your.name@your.domain",
    password: "pa55word",
    tls: :if_available, # can be `:always` or `:never`
    ssl: false, # can be `true`
    retries: 1
  ```

4. Follow Bamboo [Getting Started Guide](https://github.com/thoughtbot/bamboo#getting-started)

## Contributing

Before opening a pull request, please open an issue first.

Once we've decided how to move forward with a pull request:

```
$ git clone https://github.com/fewlinesco/bamboo_smtp.git
$ cd bamboo_smtp
$ mix deps.get
$ mix test
```

Once you've made your additions and mix test passes, go ahead and open a PR!

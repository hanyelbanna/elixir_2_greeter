greeter.ex

```elixir
defmodule Greeter do
  # module attribute is assigned variable without = sign
  @author "Mark"

  def answer_1 do
    name =
      IO.gets("Hi there! What's your name?\n")
      |> String.trim()

    if name == @author do
      "Wow! #{@author} is my favorite name. I was programmed by someone named #{@author}!"
    else
      "Hi, #{name}. It's nice to meet you."
    end
  end

  def answer_2 do
    name = IO.gets("Hi there! What's your name?\n")

    case String.trim(name) do
      "Mark" ->
        "Wow! Mark is my favorite name. I was programmed by someone named Mark!"

      trimmed_name ->
        "Hi, #{trimmed_name}. It's nice to meet you."
        # trimmed_name is a variable which will accept any string to print it in the statment
    end
  end
end

```



```
$ iex  # elixir shell
iex> c "greeter.ex"

$ iex greeter.ex  # will open iex and compile greeter.ex

```


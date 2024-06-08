# URL2SQL

[PostgREST](https://github.com/PostgREST/postgrest)-like URL to SQL transformer.

```elixir
iex> IO.iodata_to_binary URL2SQL.to_select("/todos")
{"SELECT id, done, task, due FROM todos;", []}
iex> IO.iodata_to_binary URL2SQL.to_select("/people?age=lt.13")
{"SELECT ... FROM people WHERE age < ?", [13]}
```

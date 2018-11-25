# Ideas of how to implement this

In a functional fashion, have a `model` with runs some `functions` 
with some probabilities. These functions model team behaviours. For example, 

- `run_an_sprint` removes some story points (todo -> done)
- `bug_found` adds some story points
- `new_member` increments max of story points range
- `losing_a_member` decrements max of story points range
- ...

So a model can be defined as a cycle of:

- Probability, function to run
- 100%, `run_an_sprint`
- 10%, `bug_found`
- 100%, `run_an_sprint`

- ....

These probabilites will be learned as well.

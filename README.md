[![Build](https://github.com/jidicula/random-standup/actions/workflows/build.yml/badge.svg)](https://github.com/jidicula/random-standup/actions/workflows/build.yml) [![Go Reference](https://pkg.go.dev/badge/github.com/jidicula/random-standup.svg)](https://pkg.go.dev/github.com/jidicula/random-standup)

# 🎲random-standup🎲
Do you have awkward pauses in your standups because no one wants to give their
update next? Why not have a defined order? To make it fair, why not also
🎲randomize🎲 that order!

### Do you find this useful?

Star this repo!

### Do you find this *really* useful?

You can sponsor me [here](https://github.com/sponsors/jidicula)!

## Usage

1. Get the tool with `GO111MODULE=on go get github.com/jidicula/random-standup`

2. Create a team roster in a TOML file, following the format in
`example-roster.toml`:
```toml
[Subteam-1]
members = [
        "Alice",                # TOML spec allows whitespace to break arrays
        "Bob",
        "Carol",
        "David"
        ]

["Subteam 2"]                   # Keys can have whitespace in quoted strings
members = ["Erin", "Frank", "Grace", "Heidi"]
```

3. `random-standup example-roster.toml`

## Output
```
$ random-standup example-roster.toml
# 2021-03-21
## Subteam-1
David
Bob
Carol
Alice

## Subteam 2
Frank
Erin
Heidi
Grace
```

## Building from `main`

1. Clone and `cd` into the repo.
2. `go build -v`
3. `./random-standup example-roster.toml`

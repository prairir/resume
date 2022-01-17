# Ryan's Resume

## What is this?

This is my resume. I am using a resume template https://github.com/petezh/Modular-Resume . This resume template is p nice but its not perfect.

I have made some minor changes such as

- not using emojis
- pinning and only using fontawesome5
- adding some nice spaces in between sections

## Dependencies

- Earthly Build
- Docker

## Build

Run

```sh
earthly +build --file="<file name>"
```

Where `<file name>` is the file you want to compile without the `.tex`

This system has been chosen so you can have multiple templates and still use the same components

This will create a file `<file name>.pdf`

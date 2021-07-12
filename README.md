# Bartib

Bartib is a time tracker for the command line. It safes a journal of all tracked activities in a plaintext file.

## Build

Build it with cargo:

```
cargo build --release
```

## The `.bartib` file

Bartib safes a journal of all tracked activities in a plaintext file. The file can either be specified via the `-f / --file` cli option or as a `BARTIB_FILE` environment variable.  

## Commands

### Help

Print help information:

```
bartib -h
```

### Start a new activity

Start a new activity with a short description and an associated project:

```
bartib start -p "The name of the associated project" -d "A description of the activity"
```

This will also stop all currently running activities.

### Stop a running activity

Stops the currently running activity:

```
bartib stop
```

### List all currently running activities

```
bartib current
```

### List activities

All activities:

```
bartib list
```

Do not group activities by date:

```
bartib list --no_grouping
```

List activities in a given time range:

```
bartib list --from 2021-03-01 --to 2021-11-01
```

List activities on a given day:

```
bartib list --date 2021-05-17
```
# tag-cli

```
Usage: tag [OPTIONS] COMMAND [ARGS]...

  tag-cli: file name tag manager

  File tags:
    - are in the file name directly before the extension
    - start with '{' and end with '}'
    - consist of letters, numbers and the '-' character

  Examples:
    - myfile{my-tag-1}{my-tag-2}.txt
    - My Title Case File {My-Tag-1}{My-Tag-2}.txt

Options:
  --version  Print version.
  --help     Show this message and exit.

Commands:
  add     Add tags to files.
  clear   Clear tags from files.
  remove  Remove tags from files.
  rename  Rename a tag on files.
  set     Set tags on files.
  sort    Sort tags on files.
```

## Add

```
Usage: tag add [OPTIONS] TAGS [FILES]...

  Add tags to files.

  TAGS  comma seperated list of tags
  FILES list of files

  Examples:
    - tag add my-tag myfile.txt
    - tag add my-tag-1,my-tag-2 *.txt

Options:
  -v, --verbose  Print additional output.
  -d, --debug    Make no changes to the file system.
  --help         Show this message and exit.
```

## Clear

```
Usage: tag clear [OPTIONS] [FILES]...

  Clear tags from files.

  FILES list of files

  Examples:
    - tag clear myfile{my-tag}.txt
    - tag clear *.txt

Options:
  -v, --verbose  Print additional output.
  -d, --debug    Make no changes to the file system.
  --help         Show this message and exit.
```

## Remove

```
Usage: tag remove [OPTIONS] TAGS [FILES]...

  Remove tags from files.

  TAGS  comma seperated list of tags
  FILES list of files

  Examples:
    - tag remove my-tag myfile{my-tag}.txt
    - tag remove my-tag-1,my-tag-2 *.txt

Options:
  -v, --verbose  Print additional output.
  -d, --debug    Make no changes to the file system.
  --help         Show this message and exit.
```

## Rename

```
Usage: tag rename [OPTIONS] OLD_TAG NEW_TAG [FILES]...

  Rename a tag on files.

  OLD_TAG current tag name
  NEW_TAG new tag name
  FILES list of files

  Examples:
    - tag rename my-tag my-new-tag myfile{my-tag}.txt
    - tag rename my-tag my-new-tag *.txt

Options:
  -v, --verbose  Print additional output.
  -d, --debug    Make no changes to the file system.
  --help         Show this message and exit.
```

## Set

```
Usage: tag set [OPTIONS] TAGS [FILES]...

  Set tags on files.

  Add and remove tags to ensure each file has the supplied tags and only the
  supplied tags.

  TAGS  comma seperated list of tags
  FILES list of files

  Examples:
    - tag set my-tag myfile{my-tag}.txt
    - tag set my-tag-1,my-tag-2 *.txt

Options:
  -v, --verbose  Print additional output.
  -d, --debug    Make no changes to the file system.
  --help         Show this message and exit.
```

## Sort

```
Usage: tag sort [OPTIONS] [FILES]...

  Sort tags on files.

  FILES list of files

  Examples:
    - tag sort myfile{my-tag-2}{my-tag-1}.txt
    - tag sort *.txt

Options:
  -v, --verbose  Print additional output.
  -d, --debug    Make no changes to the file system.
  --help         Show this message and exit.
```

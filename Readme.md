
# name

  description

## Installation

```
$ npm install name
```

## Example

```js
var sql = escape('INSERT INTO %I VALUES(%L)', 'books', "O'Reilly");
console.log(sql);
```

yields:

```
INSERT INTO books VALUES('O''Reilly')
```

## API

### escape(fmt, ...)

 Format the given arguments.

### escape.string(val)

  Format as a simple string.

### escape.ident(val)

  Format as an identifier.

### escape.literal(val)

  Format as a literal.

## Formats

- `%s` formats the argument value as a simple string. A null value is treated as an empty string.
- `%I` treats the argument value as an SQL identifier, double-quoting it if necessary. It is an error for the value to be null.
- `%L` quotes the argument value as an SQL literal. A null value is displayed as the string NULL, without quotes.
- `%%` In addition to the format specifiers described above, the special sequence %% may be used to output a literal % character.

# License

  MIT
[@serenity-is/corelib](../README.md) / parseHourAndMin

# Function: parseHourAndMin()

> **parseHourAndMin**(`value`): `number`

Parses a time string in the format "hh:mm" into a number containing number of minutes.
Returns NaN if the hours not in range 0-23 or minutes not in range 0-59.

## Parameters

### value

`string`

The string to parse.

## Returns

`number`

## Defined in

[src/q/formatting-compat.ts:62](https://github.com/serenity-is/serenity/blob/master/packages/corelib/src/q/formatting-compat.ts#L62)

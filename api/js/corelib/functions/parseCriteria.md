[@serenity-is/corelib](../README.md) / parseCriteria

# Function: parseCriteria()

## Call Signature

> **parseCriteria**(`expression`, `params`?): `any`[]

Parses a criteria expression to Serenity Criteria array format.
The string may optionally contain parameters like `A >= @p1 and B < @p2`.

### Parameters

#### expression

`string`

The criteria expression.

#### params?

`any`

The dictionary containing parameter values like { p1: 10, p2: 20 }.

### Returns

`any`[]

### Example

```ts
`parseCriteria('A >= @p1 and B < @p2', { p1: 5, p2: 4 }) // [[[a], '>=' 5], 'and', [[b], '<', 4]]`
```

### Defined in

[src/base/criteria.ts:694](https://github.com/serenity-is/serenity/blob/master/packages/corelib/src/base/criteria.ts#L694)

## Call Signature

> **parseCriteria**(`strings`, ...`values`): `any`[]

Parses a criteria expression to Serenity Criteria array format.
The expression may contain parameter placeholders like `A >= ${p1}`
where p1 is a variable in the scope.

### Parameters

#### strings

`TemplateStringsArray`

The string fragments.

#### values

...`any`[]

The tagged template arguments.

### Returns

`any`[]

### Example

```ts
var a = 5, b = 4;
parseCriteria`A >= ${a} and B < ${b}` // [[[a], '>=' 5], 'and', [[b], '<', 4]]
```

### Defined in

[src/base/criteria.ts:705](https://github.com/serenity-is/serenity/blob/master/packages/corelib/src/base/criteria.ts#L705)

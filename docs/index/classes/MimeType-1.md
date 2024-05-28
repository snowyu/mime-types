[**mime-type**](../../README.md) • **Docs**

***

[mime-type](../../modules.md) / [index](../README-1.md) / MimeType

# Class: MimeType

Constructs a MimeType object to manage MIME types and their associated extensions.

## Param

An initial database containing MIME type mappings.

## Param

A flag specifying how to handle duplicate MIME type entries.
    If provided, it should be one of:
      - `dupDefault: 0`: Default strategy that resolves duplicates based on source priority.
        See the description for details on this strategy.
      - `dupSkip: 1`: Skip adding the new MIME type if a duplicate entry already exists.
      - `dupOverwrite: 2`: Replace the existing MIME type with the new one if a duplicate is found.
      - `dupAppend: 3`: Add the new MIME type to the end of the existing ones if a duplicate is encountered.
    If not specified, it defaults to the `dupDefault` strategy,
    The `dupDefault` strategy works as follows:
      - If the existing MIME type is 'application/octet-stream', it's not overwritten.
      - If sources are equal and the existing type starts with 'application/', it's preserved.
      - Otherwise, if the new source is considered more authoritative (earlier in the `refSources` array),
        the new type overwrites the old one. The `refSources` array may include server configurations
        and standards bodies, such as ['nginx', 'apache', undefined, 'iana'], with `undefined` representing
        an unspecified or less authoritative source.

## Constructors

### new MimeType()

> **new MimeType**(`db`, `duplicationProcessWay`?): [`MimeType`](MimeType-1.md)

Constructs a MimeType object to manage MIME types and their associated extensions.

#### Parameters

• **db**: `any`

An initial database containing MIME type mappings.

• **duplicationProcessWay?**: `number`

A flag specifying how to handle duplicate MIME type entries.
    If provided, it should be one of:
      - `dupDefault: 0`: Default strategy that resolves duplicates based on source priority.
        See the description for details on this strategy.
      - `dupSkip: 1`: Skip adding the new MIME type if a duplicate entry already exists.
      - `dupOverwrite: 2`: Replace the existing MIME type with the new one if a duplicate is found.
      - `dupAppend: 3`: Add the new MIME type to the end of the existing ones if a duplicate is encountered.
    If not specified, it defaults to the `dupDefault` strategy,
    The `dupDefault` strategy works as follows:
      - If the existing MIME type is 'application/octet-stream', it's not overwritten.
      - If sources are equal and the existing type starts with 'application/', it's preserved.
      - Otherwise, if the new source is considered more authoritative (earlier in the `refSources` array),
        the new type overwrites the old one. The `refSources` array may include server configurations
        and standards bodies, such as ['nginx', 'apache', undefined, 'iana'], with `undefined` representing
        an unspecified or less authoritative source.

#### Returns

[`MimeType`](MimeType-1.md)

#### Source

[src/index.js:35](https://github.com/snowyu/mime-type.js/blob/c0a55571f1328e6897811c459cdccf557dee4c6f/src/index.js#L35)

## Properties

### dup

> **dup**: `number`

#### Source

[src/index.js:55](https://github.com/snowyu/mime-type.js/blob/c0a55571f1328e6897811c459cdccf557dee4c6f/src/index.js#L55)

***

### dupAppend

> **dupAppend**: `number`

#### Source

[src/index.js:14](https://github.com/snowyu/mime-type.js/blob/c0a55571f1328e6897811c459cdccf557dee4c6f/src/index.js#L14)

***

### dupDefault

> **dupDefault**: `number`

#### Source

[src/index.js:11](https://github.com/snowyu/mime-type.js/blob/c0a55571f1328e6897811c459cdccf557dee4c6f/src/index.js#L11)

***

### dupOverwrite

> **dupOverwrite**: `number`

#### Source

[src/index.js:13](https://github.com/snowyu/mime-type.js/blob/c0a55571f1328e6897811c459cdccf557dee4c6f/src/index.js#L13)

***

### dupSkip

> **dupSkip**: `number`

#### Source

[src/index.js:12](https://github.com/snowyu/mime-type.js/blob/c0a55571f1328e6897811c459cdccf557dee4c6f/src/index.js#L12)

***

### exist()

> **exist**: (`v`) => `boolean`

Determines whether an object has a property with the specified name.

#### Parameters

• **v**: `PropertyKey`

A property name.

#### Returns

`boolean`

#### Source

[src/index.js:178](https://github.com/snowyu/mime-type.js/blob/c0a55571f1328e6897811c459cdccf557dee4c6f/src/index.js#L178)

## Methods

### charset()

> **charset**(`type`): `any`

#### Parameters

• **type**: `any`

#### Returns

`any`

#### Source

[src/index.js:69](https://github.com/snowyu/mime-type.js/blob/c0a55571f1328e6897811c459cdccf557dee4c6f/src/index.js#L69)

***

### clear()

> **clear**(`filter`): `number`

#### Parameters

• **filter**: `any`

#### Returns

`number`

#### Source

[src/index.js:316](https://github.com/snowyu/mime-type.js/blob/c0a55571f1328e6897811c459cdccf557dee4c6f/src/index.js#L316)

***

### contentType()

> **contentType**(`str`): `any`

#### Parameters

• **str**: `any`

#### Returns

`any`

#### Source

[src/index.js:94](https://github.com/snowyu/mime-type.js/blob/c0a55571f1328e6897811c459cdccf557dee4c6f/src/index.js#L94)

***

### define()

> **define**(`type`, `mime`, `dup`): `any`[]

#### Parameters

• **type**: `any`

• **mime**: `any`

• **dup**: `any`

#### Returns

`any`[]

#### Source

[src/index.js:202](https://github.com/snowyu/mime-type.js/blob/c0a55571f1328e6897811c459cdccf557dee4c6f/src/index.js#L202)

***

### delete()

> **delete**(`type`): `boolean`

#### Parameters

• **type**: `any`

#### Returns

`boolean`

#### Source

[src/index.js:288](https://github.com/snowyu/mime-type.js/blob/c0a55571f1328e6897811c459cdccf557dee4c6f/src/index.js#L288)

***

### extension()

> **extension**(`type`): `any`

#### Parameters

• **type**: `any`

#### Returns

`any`

#### Source

[src/index.js:118](https://github.com/snowyu/mime-type.js/blob/c0a55571f1328e6897811c459cdccf557dee4c6f/src/index.js#L118)

***

### glob()

> **glob**(`pattern`): `string`[]

#### Parameters

• **pattern**: `any`

#### Returns

`string`[]

#### Source

[src/index.js:161](https://github.com/snowyu/mime-type.js/blob/c0a55571f1328e6897811c459cdccf557dee4c6f/src/index.js#L161)

***

### load()

> **load**(`mimes`, `duplicationProcessWay`): `number`

#### Parameters

• **mimes**: `any`

• **duplicationProcessWay**: `any`

#### Returns

`number`

#### Source

[src/index.js:269](https://github.com/snowyu/mime-type.js/blob/c0a55571f1328e6897811c459cdccf557dee4c6f/src/index.js#L269)

***

### lookup()

> **lookup**(`aPath`): `any`

#### Parameters

• **aPath**: `any`

#### Returns

`any`

#### Source

[src/index.js:137](https://github.com/snowyu/mime-type.js/blob/c0a55571f1328e6897811c459cdccf557dee4c6f/src/index.js#L137)
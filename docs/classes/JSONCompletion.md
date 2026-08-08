[@xdavidwu/codemirror-json-schema](../README.md) / JSONCompletion

# Class: JSONCompletion

## Table of contents

### Constructors

- [constructor](JSONCompletion.md#constructor)

### Methods

- [addBooleanValueCompletion](JSONCompletion.md#addbooleanvaluecompletion)
- [addDefaultValueCompletions](JSONCompletion.md#adddefaultvaluecompletions)
- [addEnumValueCompletions](JSONCompletion.md#addenumvaluecompletions)
- [addNullValueCompletion](JSONCompletion.md#addnullvaluecompletion)
- [addSchemaValueCompletions](JSONCompletion.md#addschemavaluecompletions)
- [applySnippetCompletion](JSONCompletion.md#applysnippetcompletion)
- [collectTypes](JSONCompletion.md#collecttypes)
- [doComplete](JSONCompletion.md#docomplete)
- [doCompleteForSchema](JSONCompletion.md#docompleteforschema)
- [extendedRegExp](JSONCompletion.md#extendedregexp)
- [getAppliedValue](JSONCompletion.md#getappliedvalue)
- [getInsertTextForGuessedValue](JSONCompletion.md#getinserttextforguessedvalue)
- [getInsertTextForPlainText](JSONCompletion.md#getinserttextforplaintext)
- [getInsertTextForProperty](JSONCompletion.md#getinserttextforproperty)
- [getInsertTextForPropertyName](JSONCompletion.md#getinserttextforpropertyname)
- [getInsertTextForString](JSONCompletion.md#getinserttextforstring)
- [getInsertTextForValue](JSONCompletion.md#getinserttextforvalue)
- [getPropertyCompletions](JSONCompletion.md#getpropertycompletions)
- [getSchemas](JSONCompletion.md#getschemas)
- [getValueCompletions](JSONCompletion.md#getvaluecompletions)
- [getValueFromLabel](JSONCompletion.md#getvaluefromlabel)

### Properties

- [formatInfo](JSONCompletion.md#formatinfo)
- [laxSchema](JSONCompletion.md#laxschema)
- [mode](JSONCompletion.md#mode)
- [opts](JSONCompletion.md#opts)
- [originalSchema](JSONCompletion.md#originalschema)
- [parser](JSONCompletion.md#parser)
- [schema](JSONCompletion.md#schema)

## Constructors

### constructor

• **new JSONCompletion**(`opts`)

#### Parameters

| Name   | Type                                                              |
| :----- | :---------------------------------------------------------------- |
| `opts` | [`JSONCompletionOptions`](../interfaces/JSONCompletionOptions.md) |

#### Defined in

[features/completion.ts:94](https://github.com/xdavidwu/codemirror-json-schema/blob/e1ee951/src/features/completion.ts#L94)

## Methods

### addBooleanValueCompletion

▸ `Private` **addBooleanValueCompletion**(`value`, `collector`): `void`

#### Parameters

| Name        | Type                  |
| :---------- | :-------------------- |
| `value`     | `boolean`             |
| `collector` | `CompletionCollector` |

#### Returns

`void`

#### Defined in

[features/completion.ts:867](https://github.com/xdavidwu/codemirror-json-schema/blob/e1ee951/src/features/completion.ts#L867)

---

### addDefaultValueCompletions

▸ `Private` **addDefaultValueCompletions**(`schema`, `collector`, `arrayDepth?`): `void`

#### Parameters

| Name         | Type                  | Default value |
| :----------- | :-------------------- | :------------ |
| `schema`     | `JSONSchema7`         | `undefined`   |
| `collector`  | `CompletionCollector` | `undefined`   |
| `arrayDepth` | `number`              | `0`           |

#### Returns

`void`

#### Defined in

[features/completion.ts:791](https://github.com/xdavidwu/codemirror-json-schema/blob/e1ee951/src/features/completion.ts#L791)

---

### addEnumValueCompletions

▸ `Private` **addEnumValueCompletions**(`schema`, `collector`): `void`

#### Parameters

| Name        | Type                  |
| :---------- | :-------------------- |
| `schema`    | `JSONSchema7`         |
| `collector` | `CompletionCollector` |

#### Returns

`void`

#### Defined in

[features/completion.ts:837](https://github.com/xdavidwu/codemirror-json-schema/blob/e1ee951/src/features/completion.ts#L837)

---

### addNullValueCompletion

▸ `Private` **addNullValueCompletion**(`collector`): `void`

#### Parameters

| Name        | Type                  |
| :---------- | :-------------------- |
| `collector` | `CompletionCollector` |

#### Returns

`void`

#### Defined in

[features/completion.ts:877](https://github.com/xdavidwu/codemirror-json-schema/blob/e1ee951/src/features/completion.ts#L877)

---

### addSchemaValueCompletions

▸ `Private` **addSchemaValueCompletions**(`schema`, `types`, `collector`): `void`

#### Parameters

| Name        | Type                    |
| :---------- | :---------------------- |
| `schema`    | `JSONSchema7Definition` |
| `types`     | `Object`                |
| `collector` | `CompletionCollector`   |

#### Returns

`void`

#### Defined in

[features/completion.ts:762](https://github.com/xdavidwu/codemirror-json-schema/blob/e1ee951/src/features/completion.ts#L762)

---

### applySnippetCompletion

▸ `Private` **applySnippetCompletion**(`completion`): `Completion`

#### Parameters

| Name         | Type         |
| :----------- | :----------- |
| `completion` | `Completion` |

#### Returns

`Completion`

#### Defined in

[features/completion.ts:309](https://github.com/xdavidwu/codemirror-json-schema/blob/e1ee951/src/features/completion.ts#L309)

---

### collectTypes

▸ `Private` **collectTypes**(`schema`, `types`): `void`

#### Parameters

| Name     | Type          |
| :------- | :------------ |
| `schema` | `JSONSchema7` |
| `types`  | `Object`      |

#### Returns

`void`

#### Defined in

[features/completion.ts:884](https://github.com/xdavidwu/codemirror-json-schema/blob/e1ee951/src/features/completion.ts#L884)

---

### doComplete

▸ **doComplete**(`ctx`): `never`[] \| `CompletionResult`

#### Parameters

| Name  | Type                |
| :---- | :------------------ |
| `ctx` | `CompletionContext` |

#### Returns

`never`[] \| `CompletionResult`

#### Defined in

[features/completion.ts:100](https://github.com/xdavidwu/codemirror-json-schema/blob/e1ee951/src/features/completion.ts#L100)

---

### doCompleteForSchema

▸ `Private` **doCompleteForSchema**(`ctx`, `rootSchema`): `CompletionResult`

#### Parameters

| Name         | Type                |
| :----------- | :------------------ |
| `ctx`        | `CompletionContext` |
| `rootSchema` | `JSONSchema7`       |

#### Returns

`CompletionResult`

#### Defined in

[features/completion.ts:132](https://github.com/xdavidwu/codemirror-json-schema/blob/e1ee951/src/features/completion.ts#L132)

---

### extendedRegExp

▸ `Private` **extendedRegExp**(`pattern`): `undefined` \| `RegExp`

#### Parameters

| Name      | Type     |
| :-------- | :------- |
| `pattern` | `string` |

#### Returns

`undefined` \| `RegExp`

#### Defined in

[features/completion.ts:1049](https://github.com/xdavidwu/codemirror-json-schema/blob/e1ee951/src/features/completion.ts#L1049)

---

### getAppliedValue

▸ `Private` **getAppliedValue**(`value`): `Object`

#### Parameters

| Name    | Type  |
| :------ | :---- |
| `value` | `any` |

#### Returns

`Object`

| Name    | Type     |
| :------ | :------- |
| `apply` | `string` |
| `label` | `string` |

#### Defined in

[features/completion.ts:1024](https://github.com/xdavidwu/codemirror-json-schema/blob/e1ee951/src/features/completion.ts#L1024)

---

### getInsertTextForGuessedValue

▸ `Private` **getInsertTextForGuessedValue**(`value`, `separatorAfter?`): `string`

#### Parameters

| Name             | Type     | Default value |
| :--------------- | :------- | :------------ |
| `value`          | `any`    | `undefined`   |
| `separatorAfter` | `string` | `""`          |

#### Returns

`string`

#### Defined in

[features/completion.ts:576](https://github.com/xdavidwu/codemirror-json-schema/blob/e1ee951/src/features/completion.ts#L576)

---

### getInsertTextForPlainText

▸ `Private` **getInsertTextForPlainText**(`text`): `string`

#### Parameters

| Name   | Type     |
| :----- | :------- |
| `text` | `string` |

#### Returns

`string`

#### Defined in

[features/completion.ts:599](https://github.com/xdavidwu/codemirror-json-schema/blob/e1ee951/src/features/completion.ts#L599)

---

### getInsertTextForProperty

▸ `Private` **getInsertTextForProperty**(`key`, `addValue`, `rawWord`, `rootSchema`, `propertySchema?`): `string`

#### Parameters

| Name              | Type                    |
| :---------------- | :---------------------- |
| `key`             | `string`                |
| `addValue`        | `boolean`               |
| `rawWord`         | `string`                |
| `rootSchema`      | `JSONSchema7`           |
| `propertySchema?` | `JSONSchema7Definition` |

#### Returns

`string`

#### Defined in

[features/completion.ts:428](https://github.com/xdavidwu/codemirror-json-schema/blob/e1ee951/src/features/completion.ts#L428)

---

### getInsertTextForPropertyName

▸ `Private` **getInsertTextForPropertyName**(`key`, `rawWord`): `string`

#### Parameters

| Name      | Type     |
| :-------- | :------- |
| `key`     | `string` |
| `rawWord` | `string` |

#### Returns

`string`

#### Defined in

[features/completion.ts:547](https://github.com/xdavidwu/codemirror-json-schema/blob/e1ee951/src/features/completion.ts#L547)

---

### getInsertTextForString

▸ `Private` **getInsertTextForString**(`value`, `prf?`): `string`

#### Parameters

| Name    | Type     | Default value |
| :------ | :------- | :------------ |
| `value` | `string` | `undefined`   |
| `prf`   | `string` | `"#"`         |

#### Returns

`string`

#### Defined in

[features/completion.ts:564](https://github.com/xdavidwu/codemirror-json-schema/blob/e1ee951/src/features/completion.ts#L564)

---

### getInsertTextForValue

▸ `Private` **getInsertTextForValue**(`value`, `separatorAfter`): `string`

#### Parameters

| Name             | Type     |
| :--------------- | :------- |
| `value`          | `any`    |
| `separatorAfter` | `string` |

#### Returns

`string`

#### Defined in

[features/completion.ts:603](https://github.com/xdavidwu/codemirror-json-schema/blob/e1ee951/src/features/completion.ts#L603)

---

### getPropertyCompletions

▸ `Private` **getPropertyCompletions**(`rootSchema`, `ctx`, `node`, `collector`, `addValue`, `rawWord`): `void`

#### Parameters

| Name         | Type                  |
| :----------- | :-------------------- |
| `rootSchema` | `JSONSchema7`         |
| `ctx`        | `CompletionContext`   |
| `node`       | `SyntaxNode`          |
| `collector`  | `CompletionCollector` |
| `addValue`   | `boolean`             |
| `rawWord`    | `string`              |

#### Returns

`void`

#### Defined in

[features/completion.ts:318](https://github.com/xdavidwu/codemirror-json-schema/blob/e1ee951/src/features/completion.ts#L318)

---

### getSchemas

▸ `Private` **getSchemas**(`rootSchema`, `ctx`): `JSONSchema7Definition`[]

#### Parameters

| Name         | Type                |
| :----------- | :------------------ |
| `rootSchema` | `JSONSchema7`       |
| `ctx`        | `CompletionContext` |

#### Returns

`JSONSchema7Definition`[]

#### Defined in

[features/completion.ts:899](https://github.com/xdavidwu/codemirror-json-schema/blob/e1ee951/src/features/completion.ts#L899)

---

### getValueCompletions

▸ `Private` **getValueCompletions**(`rootSchema`, `ctx`, `types`, `collector`): `undefined` \| \{ `valuePrefix`: `string` }

#### Parameters

| Name         | Type                  |
| :----------- | :-------------------- |
| `rootSchema` | `JSONSchema7`         |
| `ctx`        | `CompletionContext`   |
| `types`      | `Object`              |
| `collector`  | `CompletionCollector` |

#### Returns

`undefined` \| \{ `valuePrefix`: `string` }

#### Defined in

[features/completion.ts:613](https://github.com/xdavidwu/codemirror-json-schema/blob/e1ee951/src/features/completion.ts#L613)

---

### getValueFromLabel

▸ `Private` **getValueFromLabel**(`value`): `string`

#### Parameters

| Name    | Type  |
| :------ | :---- |
| `value` | `any` |

#### Returns

`string`

#### Defined in

[features/completion.ts:1045](https://github.com/xdavidwu/codemirror-json-schema/blob/e1ee951/src/features/completion.ts#L1045)

## Properties

### formatInfo

• `Private` **formatInfo**: (`description`: `string`) => `HTMLElement` = `defaultFormatInfo`

#### Type declaration

▸ (`description`): `HTMLElement`

##### Parameters

| Name          | Type     |
| :------------ | :------- |
| `description` | `string` |

##### Returns

`HTMLElement`

#### Defined in

[features/completion.ts:90](https://github.com/xdavidwu/codemirror-json-schema/blob/e1ee951/src/features/completion.ts#L90)

---

### laxSchema

• `Private` **laxSchema**: `null` \| `JSONSchema7` = `null`

Inlined (expanded) top-level $ref if present.
Does not contain any required properties and allows any additional properties everywhere.

#### Defined in

[features/completion.ts:87](https://github.com/xdavidwu/codemirror-json-schema/blob/e1ee951/src/features/completion.ts#L87)

---

### mode

• `Private` **mode**: `JSONMode` = `MODES.JSON`

#### Defined in

[features/completion.ts:88](https://github.com/xdavidwu/codemirror-json-schema/blob/e1ee951/src/features/completion.ts#L88)

---

### opts

• `Private` **opts**: [`JSONCompletionOptions`](../interfaces/JSONCompletionOptions.md)

#### Defined in

[features/completion.ts:94](https://github.com/xdavidwu/codemirror-json-schema/blob/e1ee951/src/features/completion.ts#L94)

---

### originalSchema

• `Private` **originalSchema**: `null` \| `JSONSchema7` = `null`

#### Defined in

[features/completion.ts:78](https://github.com/xdavidwu/codemirror-json-schema/blob/e1ee951/src/features/completion.ts#L78)

---

### parser

• `Private` **parser**: `DocumentParser`

#### Defined in

[features/completion.ts:89](https://github.com/xdavidwu/codemirror-json-schema/blob/e1ee951/src/features/completion.ts#L89)

---

### schema

• `Private` **schema**: `null` \| `JSONSchema7` = `null`

Inlined (expanded) top-level $ref if present.

#### Defined in

[features/completion.ts:82](https://github.com/xdavidwu/codemirror-json-schema/blob/e1ee951/src/features/completion.ts#L82)

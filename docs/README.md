codemirror-json-schema

# codemirror-json-schema

## Table of contents

### Bundled Codemirror Extensions

- [jsonSchema](README.md#jsonschema)

### Codemirror Extensions

- [jsonCompletion](README.md#jsoncompletion)
- [jsonSchemaHover](README.md#jsonschemahover)
- [jsonSchemaLinter](README.md#jsonschemalinter)

### Utilities

- [getJsonPointers](README.md#getjsonpointers)
- [jsonPointerForPosition](README.md#jsonpointerforposition)
- [parseJSONDocument](README.md#parsejsondocument)
- [parseJSONDocumentState](README.md#parsejsondocumentstate)

### Functions

- [getJSONSchema](README.md#getjsonschema)
- [getJsonPointerAt](README.md#getjsonpointerat)
- [handleRefresh](README.md#handlerefresh)
- [resolveTokenName](README.md#resolvetokenname)
- [stateExtensions](README.md#stateextensions)
- [updateSchema](README.md#updateschema)

### Interfaces

- [JSONValidationOptions](interfaces/JSONValidationOptions.md)

### Type Aliases

- [CursorData](README.md#cursordata)
- [FoundCursorData](README.md#foundcursordata)
- [HoverOptions](README.md#hoveroptions)
- [JSONPartialPointerData](README.md#jsonpartialpointerdata)
- [JSONPointerData](README.md#jsonpointerdata)
- [JSONPointersMap](README.md#jsonpointersmap)

### Variables

- [schemaStateField](README.md#schemastatefield)

## Bundled Codemirror Extensions

### jsonSchema

▸ **jsonSchema**(`schema?`): `Extension`[]

Full featured cm6 extension for json, including `@codemirror/lang-json`

#### Parameters

| Name | Type |
| :------ | :------ |
| `schema?` | `JSONSchema7` |

#### Returns

`Extension`[]

#### Defined in

[bundled.ts:15](https://github.com/acao/codemirror-json-schema/blob/8b311fe/src/bundled.ts#L15)

## Codemirror Extensions

### jsonCompletion

▸ **jsonCompletion**(`opts?`): (`ctx`: `CompletionContext`) => `CompletionResult` \| `never`[]

provides a JSON schema enabled autocomplete extension for codemirror

#### Parameters

| Name | Type |
| :------ | :------ |
| `opts` | `JSONCompletionOptions` |

#### Returns

`fn`

▸ (`ctx`): `CompletionResult` \| `never`[]

##### Parameters

| Name | Type |
| :------ | :------ |
| `ctx` | `CompletionContext` |

##### Returns

`CompletionResult` \| `never`[]

#### Defined in

[json-completion.ts:936](https://github.com/acao/codemirror-json-schema/blob/8b311fe/src/json-completion.ts#L936)

___

### jsonSchemaHover

▸ **jsonSchemaHover**(`options?`): (`view`: `EditorView`, `pos`: `number`, `side`: `Side`) => `Promise`<``null`` \| `Tooltip`\>

provides a JSON schema enabled tooltip extension for codemirror

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`HoverOptions`](README.md#hoveroptions) |

#### Returns

`fn`

▸ (`view`, `pos`, `side`): `Promise`<``null`` \| `Tooltip`\>

##### Parameters

| Name | Type |
| :------ | :------ |
| `view` | `EditorView` |
| `pos` | `number` |
| `side` | `Side` |

##### Returns

`Promise`<``null`` \| `Tooltip`\>

#### Defined in

[json-hover.ts:45](https://github.com/acao/codemirror-json-schema/blob/8b311fe/src/json-hover.ts#L45)

___

### jsonSchemaLinter

▸ **jsonSchemaLinter**(`options?`): (`view`: `EditorView`) => `Diagnostic`[]

Helper for simpler class instantiaton

#### Parameters

| Name | Type |
| :------ | :------ |
| `options?` | [`JSONValidationOptions`](interfaces/JSONValidationOptions.md) |

#### Returns

`fn`

▸ (`view`): `Diagnostic`[]

##### Parameters

| Name | Type |
| :------ | :------ |
| `view` | `EditorView` |

##### Returns

`Diagnostic`[]

#### Defined in

[json-validation.ts:58](https://github.com/acao/codemirror-json-schema/blob/8b311fe/src/json-validation.ts#L58)

## Utilities

### getJsonPointers

▸ **getJsonPointers**(`state`, `mode`): [`JSONPointersMap`](README.md#jsonpointersmap)

retrieve a Map of all the json pointers in a document

#### Parameters

| Name | Type |
| :------ | :------ |
| `state` | `EditorState` |
| `mode` | `JSONMode` |

#### Returns

[`JSONPointersMap`](README.md#jsonpointersmap)

#### Defined in

[utils/jsonPointers.ts:85](https://github.com/acao/codemirror-json-schema/blob/8b311fe/src/utils/jsonPointers.ts#L85)

___

### jsonPointerForPosition

▸ **jsonPointerForPosition**(`state`, `pos`, `side?`, `mode`): `string`

retrieve a JSON pointer for a given position in the editor

#### Parameters

| Name | Type | Default value |
| :------ | :------ | :------ |
| `state` | `EditorState` | `undefined` |
| `pos` | `number` | `undefined` |
| `side` | `Side` | `-1` |
| `mode` | `JSONMode` | `undefined` |

#### Returns

`string`

#### Defined in

[utils/jsonPointers.ts:68](https://github.com/acao/codemirror-json-schema/blob/8b311fe/src/utils/jsonPointers.ts#L68)

___

### parseJSONDocument

▸ **parseJSONDocument**(`jsonString`): `Object`

Mimics the behavior of `json-source-map`'s `parseJSONDocument` function using codemirror EditorState

#### Parameters

| Name | Type |
| :------ | :------ |
| `jsonString` | `string` |

#### Returns

`Object`

| Name | Type |
| :------ | :------ |
| `data` | `any` |
| `pointers` | [`JSONPointersMap`](README.md#jsonpointersmap) |

#### Defined in

[utils/parseJSONDocument.ts:24](https://github.com/acao/codemirror-json-schema/blob/8b311fe/src/utils/parseJSONDocument.ts#L24)

___

### parseJSONDocumentState

▸ **parseJSONDocumentState**(`state`): `Object`

Return parsed data and json pointers for a given codemirror EditorState

#### Parameters

| Name | Type |
| :------ | :------ |
| `state` | `EditorState` |

#### Returns

`Object`

| Name | Type |
| :------ | :------ |
| `data` | `any` |
| `pointers` | [`JSONPointersMap`](README.md#jsonpointersmap) |

#### Defined in

[utils/parseJSONDocument.ts:10](https://github.com/acao/codemirror-json-schema/blob/8b311fe/src/utils/parseJSONDocument.ts#L10)

## Functions

### getJSONSchema

▸ **getJSONSchema**(`state`): `void` \| `JSONSchema7`

#### Parameters

| Name | Type |
| :------ | :------ |
| `state` | `EditorState` |

#### Returns

`void` \| `JSONSchema7`

#### Defined in

[state.ts:25](https://github.com/acao/codemirror-json-schema/blob/8b311fe/src/state.ts#L25)

___

### getJsonPointerAt

▸ **getJsonPointerAt**(`docText`, `node`, `mode`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `docText` | `Text` |
| `node` | `SyntaxNode` |
| `mode` | `JSONMode` |

#### Returns

`string`

#### Defined in

[utils/jsonPointers.ts:31](https://github.com/acao/codemirror-json-schema/blob/8b311fe/src/utils/jsonPointers.ts#L31)

___

### handleRefresh

▸ **handleRefresh**(`vu`): `boolean`

#### Parameters

| Name | Type |
| :------ | :------ |
| `vu` | `ViewUpdate` |

#### Returns

`boolean`

#### Defined in

[json-validation.ts:48](https://github.com/acao/codemirror-json-schema/blob/8b311fe/src/json-validation.ts#L48)

___

### resolveTokenName

▸ **resolveTokenName**(`nodeName`, `mode`): `string`

#### Parameters

| Name | Type |
| :------ | :------ |
| `nodeName` | `string` |
| `mode` | `JSONMode` |

#### Returns

`string`

#### Defined in

[utils/jsonPointers.ts:18](https://github.com/acao/codemirror-json-schema/blob/8b311fe/src/utils/jsonPointers.ts#L18)

___

### stateExtensions

▸ **stateExtensions**(`schema?`): `Extension`[]

#### Parameters

| Name | Type |
| :------ | :------ |
| `schema?` | `JSONSchema7` |

#### Returns

`Extension`[]

#### Defined in

[state.ts:29](https://github.com/acao/codemirror-json-schema/blob/8b311fe/src/state.ts#L29)

___

### updateSchema

▸ **updateSchema**(`view`, `schema?`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `view` | `EditorView` |
| `schema?` | `JSONSchema7` |

#### Returns

`void`

#### Defined in

[state.ts:19](https://github.com/acao/codemirror-json-schema/blob/8b311fe/src/state.ts#L19)

## Type Aliases

### CursorData

Ƭ **CursorData**: `Object`

#### Type declaration

| Name | Type |
| :------ | :------ |
| `pointer` | `string` |
| `schema?` | `JsonSchema` |

#### Defined in

[json-hover.ts:18](https://github.com/acao/codemirror-json-schema/blob/8b311fe/src/json-hover.ts#L18)

___

### FoundCursorData

Ƭ **FoundCursorData**: `Required`<[`CursorData`](README.md#cursordata)\>

#### Defined in

[json-hover.ts:20](https://github.com/acao/codemirror-json-schema/blob/8b311fe/src/json-hover.ts#L20)

___

### HoverOptions

Ƭ **HoverOptions**: `Object`

#### Type declaration

| Name | Type |
| :------ | :------ |
| `formatHover?` | (`data`: `HoverTexts`) => `HTMLElement` |
| `getHoverTexts?` | (`data`: [`FoundCursorData`](README.md#foundcursordata)) => `HoverTexts` |
| `mode?` | `JSONMode` |
| `parser?` | (`text`: `string`) => `any` |

#### Defined in

[json-hover.ts:24](https://github.com/acao/codemirror-json-schema/blob/8b311fe/src/json-hover.ts#L24)

___

### JSONPartialPointerData

Ƭ **JSONPartialPointerData**: `Object`

#### Type declaration

| Name | Type |
| :------ | :------ |
| `keyFrom` | `number` |
| `keyTo` | `number` |

#### Defined in

[types.ts:6](https://github.com/acao/codemirror-json-schema/blob/8b311fe/src/types.ts#L6)

___

### JSONPointerData

Ƭ **JSONPointerData**: `Object`

#### Type declaration

| Name | Type |
| :------ | :------ |
| `keyFrom` | `number` |
| `keyTo` | `number` |
| `valueFrom` | `number` |
| `valueTo` | `number` |

#### Defined in

[types.ts:11](https://github.com/acao/codemirror-json-schema/blob/8b311fe/src/types.ts#L11)

___

### JSONPointersMap

Ƭ **JSONPointersMap**: `Map`<`string`, [`JSONPointerData`](README.md#jsonpointerdata) \| [`JSONPartialPointerData`](README.md#jsonpartialpointerdata)\>

#### Defined in

[types.ts:20](https://github.com/acao/codemirror-json-schema/blob/8b311fe/src/types.ts#L20)

## Variables

### schemaStateField

• `Const` **schemaStateField**: `StateField`<`void` \| `JSONSchema7`\>

#### Defined in

[state.ts:6](https://github.com/acao/codemirror-json-schema/blob/8b311fe/src/state.ts#L6)

[avalanche](../README.md) › [API-AVM-Inputs](../modules/api_avm_inputs.md) › [AmountInput](api_avm_inputs.amountinput.md)

# Class: AmountInput

## Hierarchy

  ↳ [StandardAmountInput](common_inputs.standardamountinput.md)

  ↳ **AmountInput**

  ↳ [SECPTransferInput](api_avm_inputs.secptransferinput.md)

## Index

### Constructors

* [constructor](api_avm_inputs.amountinput.md#constructor)

### Properties

* [amount](api_avm_inputs.amountinput.md#protected-amount)
* [amountValue](api_avm_inputs.amountinput.md#protected-amountvalue)
* [sigCount](api_avm_inputs.amountinput.md#protected-sigcount)
* [sigIdxs](api_avm_inputs.amountinput.md#protected-sigidxs)

### Methods

* [addSignatureIdx](api_avm_inputs.amountinput.md#addsignatureidx)
* [clone](api_avm_inputs.amountinput.md#abstract-clone)
* [create](api_avm_inputs.amountinput.md#abstract-create)
* [fromBuffer](api_avm_inputs.amountinput.md#frombuffer)
* [getAmount](api_avm_inputs.amountinput.md#getamount)
* [getCredentialID](api_avm_inputs.amountinput.md#abstract-getcredentialid)
* [getInputID](api_avm_inputs.amountinput.md#abstract-getinputid)
* [getSigIdxs](api_avm_inputs.amountinput.md#getsigidxs)
* [select](api_avm_inputs.amountinput.md#select)
* [toBuffer](api_avm_inputs.amountinput.md#tobuffer)
* [toString](api_avm_inputs.amountinput.md#tostring)
* [comparator](api_avm_inputs.amountinput.md#static-comparator)

## Constructors

###  constructor

\+ **new AmountInput**(`amount`: BN): *[AmountInput](api_avm_inputs.amountinput.md)*

*Inherited from [StandardAmountInput](common_inputs.standardamountinput.md).[constructor](common_inputs.standardamountinput.md#constructor)*

*Overrides [Input](common_inputs.input.md).[constructor](common_inputs.input.md#constructor)*

*Defined in [src/common/input.ts:223](https://github.com/ava-labs/avalanchejs/blob/a2feb77/src/common/input.ts#L223)*

An [AmountInput](api_avm_inputs.amountinput.md) class which issues a payment on an assetID.

**Parameters:**

Name | Type | Default | Description |
------ | ------ | ------ | ------ |
`amount` | BN | undefined | A [BN](https://github.com/indutny/bn.js/) representing the amount in the input  |

**Returns:** *[AmountInput](api_avm_inputs.amountinput.md)*

## Properties

### `Protected` amount

• **amount**: *Buffer* = Buffer.alloc(8)

*Inherited from [StandardAmountInput](common_inputs.standardamountinput.md).[amount](common_inputs.standardamountinput.md#protected-amount)*

*Defined in [src/common/input.ts:196](https://github.com/ava-labs/avalanchejs/blob/a2feb77/src/common/input.ts#L196)*

___

### `Protected` amountValue

• **amountValue**: *BN* = new BN(0)

*Inherited from [StandardAmountInput](common_inputs.standardamountinput.md).[amountValue](common_inputs.standardamountinput.md#protected-amountvalue)*

*Defined in [src/common/input.ts:198](https://github.com/ava-labs/avalanchejs/blob/a2feb77/src/common/input.ts#L198)*

___

### `Protected` sigCount

• **sigCount**: *Buffer* = Buffer.alloc(4)

*Inherited from [Input](common_inputs.input.md).[sigCount](common_inputs.input.md#protected-sigcount)*

*Defined in [src/common/input.ts:17](https://github.com/ava-labs/avalanchejs/blob/a2feb77/src/common/input.ts#L17)*

___

### `Protected` sigIdxs

• **sigIdxs**: *Array‹[SigIdx](common_signature.sigidx.md)›* = []

*Inherited from [Input](common_inputs.input.md).[sigIdxs](common_inputs.input.md#protected-sigidxs)*

*Defined in [src/common/input.ts:19](https://github.com/ava-labs/avalanchejs/blob/a2feb77/src/common/input.ts#L19)*

## Methods

###  addSignatureIdx

▸ **addSignatureIdx**(`addressIdx`: number, `address`: Buffer): *void*

*Inherited from [Input](common_inputs.input.md).[addSignatureIdx](common_inputs.input.md#addsignatureidx)*

*Defined in [src/common/input.ts:36](https://github.com/ava-labs/avalanchejs/blob/a2feb77/src/common/input.ts#L36)*

Creates and adds a [SigIdx](common_signature.sigidx.md) to the [Input](common_inputs.input.md).

**Parameters:**

Name | Type | Description |
------ | ------ | ------ |
`addressIdx` | number | The index of the address to reference in the signatures |
`address` | Buffer | The address of the source of the signature  |

**Returns:** *void*

___

### `Abstract` clone

▸ **clone**(): *this*

*Inherited from [Input](common_inputs.input.md).[clone](common_inputs.input.md#abstract-clone)*

*Defined in [src/common/input.ts:94](https://github.com/ava-labs/avalanchejs/blob/a2feb77/src/common/input.ts#L94)*

**Returns:** *this*

___

### `Abstract` create

▸ **create**(...`args`: any[]): *this*

*Inherited from [Input](common_inputs.input.md).[create](common_inputs.input.md#abstract-create)*

*Defined in [src/common/input.ts:96](https://github.com/ava-labs/avalanchejs/blob/a2feb77/src/common/input.ts#L96)*

**Parameters:**

Name | Type |
------ | ------ |
`...args` | any[] |

**Returns:** *this*

___

###  fromBuffer

▸ **fromBuffer**(`bytes`: Buffer, `offset`: number): *number*

*Inherited from [StandardAmountInput](common_inputs.standardamountinput.md).[fromBuffer](common_inputs.standardamountinput.md#frombuffer)*

*Overrides [Input](common_inputs.input.md).[fromBuffer](common_inputs.input.md#frombuffer)*

*Defined in [src/common/input.ts:208](https://github.com/ava-labs/avalanchejs/blob/a2feb77/src/common/input.ts#L208)*

Popuates the instance from a [Buffer](https://github.com/feross/buffer) representing the [AmountInput](api_avm_inputs.amountinput.md) and returns the size of the output.

**Parameters:**

Name | Type | Default |
------ | ------ | ------ |
`bytes` | Buffer | - |
`offset` | number | 0 |

**Returns:** *number*

___

###  getAmount

▸ **getAmount**(): *BN*

*Inherited from [StandardAmountInput](common_inputs.standardamountinput.md).[getAmount](common_inputs.standardamountinput.md#getamount)*

*Defined in [src/common/input.ts:203](https://github.com/ava-labs/avalanchejs/blob/a2feb77/src/common/input.ts#L203)*

Returns the amount as a [BN](https://github.com/indutny/bn.js/).

**Returns:** *BN*

___

### `Abstract` getCredentialID

▸ **getCredentialID**(): *number*

*Inherited from [Input](common_inputs.input.md).[getCredentialID](common_inputs.input.md#abstract-getcredentialid)*

*Defined in [src/common/input.ts:28](https://github.com/ava-labs/avalanchejs/blob/a2feb77/src/common/input.ts#L28)*

**Returns:** *number*

___

### `Abstract` getInputID

▸ **getInputID**(): *number*

*Inherited from [Input](common_inputs.input.md).[getInputID](common_inputs.input.md#abstract-getinputid)*

*Defined in [src/common/input.ts:21](https://github.com/ava-labs/avalanchejs/blob/a2feb77/src/common/input.ts#L21)*

**Returns:** *number*

___

###  getSigIdxs

▸ **getSigIdxs**(): *Array‹[SigIdx](common_signature.sigidx.md)›*

*Inherited from [Input](common_inputs.input.md).[getSigIdxs](common_inputs.input.md#getsigidxs)*

*Defined in [src/common/input.ts:26](https://github.com/ava-labs/avalanchejs/blob/a2feb77/src/common/input.ts#L26)*

Returns the array of [SigIdx](common_signature.sigidx.md) for this [Input](common_inputs.input.md)

**Returns:** *Array‹[SigIdx](common_signature.sigidx.md)›*

___

###  select

▸ **select**(`id`: number, ...`args`: any[]): *[Input](common_inputs.input.md)*

*Overrides [Input](common_inputs.input.md).[select](common_inputs.input.md#abstract-select)*

*Defined in [src/apis/avm/inputs.ts:57](https://github.com/ava-labs/avalanchejs/blob/a2feb77/src/apis/avm/inputs.ts#L57)*

**Parameters:**

Name | Type |
------ | ------ |
`id` | number |
`...args` | any[] |

**Returns:** *[Input](common_inputs.input.md)*

___

###  toBuffer

▸ **toBuffer**(): *Buffer*

*Inherited from [StandardAmountInput](common_inputs.standardamountinput.md).[toBuffer](common_inputs.standardamountinput.md#tobuffer)*

*Overrides [Input](common_inputs.input.md).[toBuffer](common_inputs.input.md#tobuffer)*

*Defined in [src/common/input.ts:218](https://github.com/ava-labs/avalanchejs/blob/a2feb77/src/common/input.ts#L218)*

Returns the buffer representing the [AmountInput](api_avm_inputs.amountinput.md) instance.

**Returns:** *Buffer*

___

###  toString

▸ **toString**(): *string*

*Inherited from [Input](common_inputs.input.md).[toString](common_inputs.input.md#tostring)*

*Defined in [src/common/input.ts:76](https://github.com/ava-labs/avalanchejs/blob/a2feb77/src/common/input.ts#L76)*

Returns a base-58 representation of the [Input](common_inputs.input.md).

**Returns:** *string*

___

### `Static` comparator

▸ **comparator**(): *function*

*Inherited from [Input](common_inputs.input.md).[comparator](common_inputs.input.md#static-comparator)*

*Defined in [src/common/input.ts:80](https://github.com/ava-labs/avalanchejs/blob/a2feb77/src/common/input.ts#L80)*

**Returns:** *function*

▸ (`a`: [Input](common_inputs.input.md), `b`: [Input](common_inputs.input.md)): *0 | 1 | -1*

**Parameters:**

Name | Type |
------ | ------ |
`a` | [Input](common_inputs.input.md) |
`b` | [Input](common_inputs.input.md) |

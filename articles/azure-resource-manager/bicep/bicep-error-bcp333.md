---
title: BCP333
description: Error/warning - The provided value (whose length will always be less than or equal to <length>) is too short to assign to a target for which the minimum allowable length is <min-length>.
ms.topic: reference
ms.custom: devx-track-bicep
ms.date: 07/15/2024
---

# Bicep error/warning code - BCP333

This error/warning occurs when an assigned string or array is shorter than the allowable length.

## Error/warning description

`The provided value (whose length will always be less than or equal to <length>) is too short to assign to a target for which the minimum allowable length is <min-length>.`

## Solution

Assign a string whose length is within the allowable range.

## Examples

The following example raises the error because the value `st` is shorter than the allowable length:

```bicep
@minLength(3)
@maxLength(10)
param storageAccountName string = 'st'
```

You can fix the error by assigning a string whose length is within the allowable range.

```bicep
@minLength(3)
@maxLength(10)
param storageAccountName string = 'myStorage'
```

## Next steps

For more information about Bicep error and warning codes, see [Bicep warnings and errors](./bicep-error-codes.md).
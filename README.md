# Quickstart for Bitasmbl project (Laravel)

## 1) Install Bitasmbl-CLI package

```bash
npm i bitasmbl-cli
```

## 2) Run bitasmbl command to set up the project

```bash
bitasmbl pull --repoUrl https://github.com/he1snber8/Bitasmbl_support-this-bitch_722_59_46 --appId 59 --repoId 46
```

## 3) Enter into the main directory and start coding!

```bash
cd Bitasmbl_support-this-bitch_722_59_46
```

## Customize requirements in a way you like

Bitasmbl organizes development into requirements. Each requirement describes a feature or implementation goal and can define suggested file locations through a `paths` array.

The `paths` property acts as a mapping guideline, helping contributors understand where related code should live.

You can customize `paths` mappings through the `bitasmbl.json` file.

{"Requirement":"Define ticket models","Paths":["**/app/Models/**","**/database/migrations/**"]}

## Requirement Evaluation

Bitasmbl includes a requirement evaluation workflow that lets contributors select a task and submit work for validation.

Run:

```bash
bitasmbl evaluate
```

Example output:

<pre>
? Available Requirements:

❯ [<span style="color:#9333ea">1</span>] <span style="color:#9333ea"> Define portfolio layout </span>            [3]
  [2] Build showcase components            [3]
  [3] Implement navigation routing         [3]
</pre>

`[x]` on the right represents the number of submission attempts remaining for a requirement.

## Example evaluation result

```php
<?php

/*
|--------------------------------------------------------------------------
| BITASMBL EVALUATION
|--------------------------------------------------------------------------
| REQUIREMENT:
| Implement product catalog API
|
| SCORE: 18/100
| STATUS: FAIL ✕
|
| INSIGHT:
| The endpoint returns static product data and does not use a model,
| controller resource, validation, database query, or service layer.
|--------------------------------------------------------------------------
*/

use Illuminate\Support\Facades\Route;

Route::get('/products', function () {
    return response()->json([
        [
            'id' => 1,
            'name' => 'Keyboard',
            'price' => 89.99,
        ],
        [
            'id' => 2,
            'name' => 'Mouse',
            'price' => 49.99,
        ],
    ]);
});
```

## Learn More

For complete command references, workflow explanations, and additional documentation, visit:

👉 [Bitasmbl Documentation](https://bitasmbl.com/docs)

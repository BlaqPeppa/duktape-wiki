# How to work with value stack types

<table>
<tr>
<th>Value stack entry type</th>
<th>duk_get_xxx()</th>
<th>duk_XXX_Xxx()</th>
<th>duk_require_xxx()</th>
<th>duk_opt_xxx()</th>
<th>duk_to_xxx()</th>
</tr>

<tr>
<td>None, index out of bounds</td>
<td>default (automatic)</td>
<td>default (explicit)</td>
<td>TypeError</td>
<td>default (explicit)</td>
<td>TypeError</td>
</tr>

<tr>
<td>undefined</td>
<td>default (automatic)</td>
<td>default (explicit)</td>
<td>TypeError</td>
<td>default (explicit)</td>
<td>coercion</td>
</tr>

<tr>
<td>null</td>
<td>default (automatic)</td>
<td>default (explicit)</td>
<td>TypeError</td>
<td>default (explicit)</td>
<td>coercion</td>
</tr>

<tr>
<td>Matching type</td>
<td>as is</td>
<td>as is</td>
<td>as is</td>
<td>as is</td>
<td>as is</td>
</tr>

<tr>
<td>Non-matching type</td>
<td>default (automatic)</td>
<td>default (explicit)</td>
<td>TypeError</td>
<td>TypeError</td>
<td>coercion</td>
</tr>

</table>

Notes:

* Integer getters do a double-to-integer coercion for the API return value.
  This coercion does not change the number on the value stack.

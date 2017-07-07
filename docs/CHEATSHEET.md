# Common Prop Cheat Sheet

<h3>Prop: <code>state</code></h3>
<strong>type: String</strong>

<table class="table table-sm table-responsive">
<thead class="thead-default">
  <tr>
    <th>Standard Values</th>
    <th><code>&lt;b-form-fieldset&gt;</code></th>
    <th><code>&lt;b-form-file&gt;</code></th>
    <th><code>&lt;b-form-select&gt;</code></th>
    <th><code>&lt;b-form-input&gt;</code></th>
    <th><code>&lt;b-form-radio&gt;</code></th>
    <th><code>&lt;b-form-checkbox&gt;</code></th>
  </tr>
</thead>
<tbody>
  <tr>
    <th><code>success</code></th>
    <td>&#x2714;</td>
    <td>&#x2716;</td>
    <td>&#x2726;</td>
    <td>&#x2731;</td>
    <td>&#x2714;</td>
    <td>&#x2726;</td>
  </tr>
  <tr>
    <th><code>danger</code></th>
    <td>&#x2714;</td>
    <td>&#x2716;</td>
    <td>&#x2726;</td>
    <td>&#x2731;</td>
    <td>&#x2714;</td>
    <td>&#x2726;</td>
  </tr>
  <tr>
    <th><code>warning</code></th>
    <td>&#x2714;</td>
    <td>&#x2716;</td>
    <td>&#x2726;</td>
    <td>&#x2731;</td>
    <td>&#x2714;</td>
    <td>&#x2726;</td>
  </tr>
</tbody>
</table>

**note:**

 - &#x2731; `<b-form-input>` (textual) the state is only used to add the indictor
icon when placed inside a `<b-form-fieldset>` which has the *same* `state` applied.
 - &#x2726; States can be aplied to `<b-form-select>` and `<b-form-checkbox>` indirectly
by placing them inside a `<b-form-fieldset>` which has a `state` applied.

<h3>Prop: <code>variant</code></h3>
<strong>type: String</strong>

<table class="table table-sm table-responsive">
<thead class="thead-default">
  <tr>
    <th>Standard Values</th>
    <th><code>&lt;b-alert&gt;</code></th>
    <th><code>&lt;b-badge&gt;</code></th>
    <th><code>&lt;b-button&gt;</code></th>
    <th><code>&lt;b-table&gt;</code></th>
    <th><code>&lt;b-card&gt;</code></th>
    <th><code>&lt;b-dropdown&gt;</code></th>
    <th><code>&lt;b-list-group-item&gt;</code></th>
    <th><code>&lt;b-navbar&gt;</code></th>
    <th><code>&lt;b-progress&gt;</code></th>
  </tr>
</thead>
<tbody>
  <tr>
    <th><code>default</code></th>
    <td>&#x2716;</td>
    <td>&#x2714;</td>
    <td>&#x2716;</td>
    <td>&#x2714;</td>
    <td> </td>
    <td>&#x2716;</td>
    <td>&#x2716;</td>
    <td>&#x2716;</td>
    <td>&#x2716;</td>
  </tr>
  <tr>
    <th><code>primary</code></th>
    <td>&#x2716;</td>
    <td>&#x2714;</td>
    <td>&#x2714;</td>
    <td>&#x2714;</td>
    <td> </td>
    <td>&#x2714;</td>
    <td>&#x2716;</td>
    <td>&#x2716;</td>
    <td>&#x2716;</td>
  </tr>
  <tr>
    <th><code>secondary</code></th>
    <td>&#x2716;</td>
    <td>&#x2716;</td>
    <td>&#x2714;</td>
    <td>&#x2714;</td>
    <td> </td>
    <td>&#x2714;</td>
    <td>&#x2716;</td>
    <td>&#x2716;</td>
    <td>&#x2716;</td>
  </tr>
  <tr>
    <th><code>success</code></th>
    <td>&#x2714;</td>
    <td>&#x2714;</td>
    <td>&#x2714;</td>
    <td>&#x2714;</td>
    <td> </td>
    <td>&#x2714;</td>
    <td>&#x2714;</td>
    <td>&#x2714;</td>
    <td>&#x2714;</td>
  </tr>
  <tr>
    <th><code>warning</code></th>
    <td>&#x2714;</td>
    <td>&#x2714;</td>
    <td>&#x2714;</td>
    <td>&#x2714;</td>
    <td> </td>
    <td>&#x2714;</td>
    <td>&#x2714;</td>
    <td>&#x2714;</td>
    <td>&#x2714;</td>
  </tr>
  <tr>
    <th><code>info</code></th>
    <td>&#x2714;</td>
    <td>&#x2714;</td>
    <td>&#x2714;</td>
    <td>&#x2714;</td>
    <td> </td>
    <td>&#x2714;</td>
    <td>&#x2714;</td>
    <td>&#x2714;</td>
    <td>&#x2714;</td>
  </tr>
  <tr>
    <th><code>danger</code></th>
    <td>&#x2714;</td>
    <td>&#x2714;</td>
    <td>&#x2714;</td>
    <td>&#x2714;</td>
    <td> </td>
    <td>&#x2714;</td>
    <td>&#x2714;</td>
    <td>&#x2714;</td>
    <td>&#x2714;</td>
  </tr>
  <tr>
    <th><code>outline-primary</code></th>
    <td>&#x2716;</td>
    <td>&#x2716;</td>
    <td>&#x2714;</d>
    <td>&#x2716;</td>
    <td> </td>
    <td>&#x2714;</td>
    <td>&#x2716;</td>
    <td>&#x2716;</td>
    <td>&#x2716;</td>
  </tr>
  <tr>
    <th><code>outline-secondary</code></th>
    <td>&#x2716;</td>
    <td>&#x2716;</td>
    <td>&#x2714;</d>
    <td>&#x2716;</td>
    <td> </td>
    <td>&#x2714;</td>
    <td>&#x2716;</td>
    <td>&#x2716;</td>
    <td>&#x2716;</td>
  </tr>
  <tr>
    <th><code>outline-success</code></th>
    <td>&#x2716;</td>
    <td>&#x2716;</td>
    <td>&#x2714;</d>
    <td>&#x2716;</td>
    <td> </td>
    <td>&#x2714;</td>
    <td>&#x2716;</td>
    <td>&#x2716;</td>
    <td>&#x2716;</td>
  </tr>
  <tr>
    <th><code>outline-warning</code></th>
    <td>&#x2716;</td>
    <td>&#x2716;</td>
    <td>&#x2714;</td>
    <td>&#x2716;</td>
    <td> </td>
    <td>&#x2714;</td>
    <td>&#x2716;</td>
    <td>&#x2716;</td>
    <td>&#x2716;</td>
  </tr>
  <tr>
    <th><code>outline-danger</code></th>
    <td>&#x2716;</td>
    <td>&#x2716;</td>
    <td>&#x2714;</td>
    <td>&#x2716;</td>
    <td> </td>
    <td>&#x2714;</td>
    <td>&#x2716;</td>
    <td>&#x2716;</td>
    <td>&#x2716;</td>
  </tr>
  <tr>
    <th><code>link</code></th>
    <td>&#x2716;</td>
    <td>&#x2716;</td>
    <td>&#x2714;</td>
    <td>&#x2716;</td>
    <td> </td>
    <td>&#x2714;</td>
    <td>&#x2716;</td>
    <td>&#x2716;</td>
    <td>&#x2716;</td>
  </tr>
</tbody>
</table>

<h3>Prop: <code>size</code>, <code>button-size</code></h3>
<strong>type: String</strong>

<table class="table table-sm table-responsive">
<thead class="thead-default">
  <tr>
    <th>Standard Values</th>
    <th><code>&lt;b-button&gt;</code></th>
    <th><code>&lt;b-form-file&gt;</code></th>
    <th><code>&lt;b-form-*&gt;</code></th>
    <th><code>&lt;b-modal&gt;</code></th>
    <th><code>&lt;b-dropdown&gt;</code></th>
    <th><code>&lt;b-nav-dropdown&gt;</code></th>
  </tr>
</thead>
<tbody>
  <tr>
    <th><code>lg</code></th>
    <td>&#x2714;</td>
    <td> </td>
    <td>&#x2714;</td>
    <td>&#x2714;</td>
    <td>&#x2714;</td>
    <td>&#x2714;</td>
  </tr>
  <tr>
    <th><code>sm</code></th>
    <td>&#x2714;</td>
    <td> </d>
    <td>&#x2714;</td>
    <td>&#x2714;</td>
    <td>&#x2714;</td>
    <td>&#x2714;</td>
  </tr>
</tbody>
</table>

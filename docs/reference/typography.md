# Markdown Extension Examples

This page demonstrates some of the built-in markdown extensions provided by VitePress.

## Syntax Highlighting

VitePress provides Syntax Highlighting powered by [Shikiji](https://github.com/antfu/shikiji), with additional features like line-highlighting:

**Input**

````md
```js{4}
export default {
  data () {
    return {
      msg: 'Highlighted!'
    }
  }
}
```
````

**Output**

```js{4}
export default {
  data () {
    return {
      msg: 'Highlighted!'
    }
  }
}
```

## Custom Containers

**Input**

```md
::: info
This is an info box.
:::

::: tip
This is a tip.
:::

::: warning
This is a warning.
:::

::: danger
This is a dangerous warning.
:::

::: details
This is a details block.
:::
```

**Output**

::: info
This is an info box.
:::

::: tip
This is a tip.
:::

::: warning
This is a warning.
:::

::: danger
This is a dangerous warning.
:::

::: details
This is a details block.
:::

## Math Equation

### Inline style

$a^2 + b^2 =c^2$

### Display style

$$
  a = \frac{b+c}{d}
$$

### Display style with custom environment

$$
  \begin{array}{lcl}
      a + b + c + d & = & e + f + \\
                    &   & g + h
  \end{array}
$$

## Lucide Icons

You can use Lucide icons directly in your markdown content.

### Basic Usage

Here's a simple heart icon: <LucideIcon name="Heart" />

### Customizing Icons

You can change the size and color:

- Default size: <LucideIcon name="AlertCircle" />
- Larger icon: <LucideIcon name="AlertCircle" size="24" />
- Colored icon: <LucideIcon name="Check" color="green" size="20" />

### Icons Inline with Text

You can place icons inline with text:

- Click the <LucideIcon name="Settings" /> icon to access settings
- Make sure to <LucideIcon name="Save" /> your work regularly
- <LucideIcon name="AlertTriangle" color="#ff9800" /> Warning: This action cannot be undone

### Available Icons

For a complete list of available icons, visit the [Lucide Icons website](https://lucide.dev/icons/).

When using an icon, use the Pascal case name of the icon (e.g., `AlertCircle` not `alert-circle`).

## More

Check out the documentation for the [full list of markdown extensions](https://vitepress.dev/guide/markdown).

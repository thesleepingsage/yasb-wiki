# Recycle Bin Widget
Recycle Bin widget is simple widget that shows the status of the recycle bin. It displays the number of items in the recycle bin and the total size of the items. The widget can be customized to show different icons and colors based on the status of the recycle bin.

| Option     | Type   | Default | Description                                                                 |
|------------|--------|---------|-----------------------------------------------------------------------------|
| `label`   | string | `{icon} {items_count} {items_size}` | Format for displaying recycle bin information. Available variables: `{icon}`, `{items_count}`, `{items_size}`. |
| `label_alt`   | string | `{icon} {items_count} {items_size}` | Alternative label format that can be toggled with right-click (or configured callback). |
| `icons` | dict | `{"bin_empty": "\udb82\ude7a","bin_filled": "\udb82\ude79"}` | Customize icons used for different recycle bin states. |
| `animation` | dict | `{'enabled': True, 'type': 'fadeInOut', 'duration': 200}` | Animation settings for the widget. |
| `container_padding` | dict | `{'top': 0, 'left': 0, 'bottom': 0, 'right': 0}` | Explicitly set padding inside widget container. |
| `callbacks` | dict | See below | Configure widget interaction callbacks. |


## Example Configuration

```yaml
  bin:
    type: "yasb.recycle_bin.RecycleBinWidget"
    options:
      label: "<span>{icon}</span> Items {items_count} ({items_size})"
      label_alt: "Items {items_count}, Total size ({items_size})"
      icons:
        bin_empty: "\udb82\ude7a"
        bin_filled: "\udb82\ude79"
      container_padding:
        left: 0
        top: 0
        right: 0
        bottom: 0
      callbacks:
        on_left: "open_bin"
        on_right: "toggle_label"
        on_middle: "empty_bin"
```

## Description of Options

- **label**: Format for displaying timer information. Available variables: `{remaining}`, `{elapsed}`, `{session}`, `{total_sessions}`, `{session_type}`.
- **label_alt**: Alternative label format that can be toggled with right-click (or configured callback).
- **icons**: Customize icons used for different recycle bin states. The default icons are:
    - **bin_empty**: Icon when the recycle bin is empty.
    - **bin_filled**: Icon when the recycle bin has items.
- **container_padding**: Set padding inside widget container for top, left, bottom and right sides.  
- **animation**: Animation settings including type and duration.
- **callbacks**: Configure what happens when clicking the widget.


## Available Callbacks

- **toggle_label**: Toggle between main and alternative label format.
- **empty_bin**: Empty the recycle bin.
- **open_bin**: Open the recycle bin.


## Available Style

```css
.recycle-bin-widget {} /*Style for widget.*/
.recycle-bin-widget .widget-container {} /*Style for widget container.*/
.recycle-bin-widget .label {} /*Style for label.*/
.recycle-bin-widget .icon {} /*Style for icon.*/
.recycle-bin-widget .label.bin-empty {} /*Style for label when bin is empty.*/
.recycle-bin-widget .label.bin-filled  {} /*Style for label when bin is filled.*/
.recycle-bin-widget .icon.bin-empty  {} /*Style for icon when bin is empty.*/
.recycle-bin-widget .icon.bin-filled  {} /*Style for icon when bin is filled.*/
```
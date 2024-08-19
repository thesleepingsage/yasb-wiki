# Battery Widget Configuration

| Option                  | Type    | Default                                      | Description                                                                 |
|-------------------------|---------|----------------------------------------------|-----------------------------------------------------------------------------|
| `label`                 | string  | `{icon}`                                     | The primary label format.                                                   |
| `label_alt`             | string  | `{percent}%` | Battery percent           | The alternative label format.                                               |
| `update_interval`       | integer | `5000`                                       | The interval in milliseconds to update the widget.                          |
| `time_remaining_natural`| boolean | `False`                                      | Whether to display the remaining time in a natural format.                  |
| `charging_options`      | dict    | `{icon_format: '{charging_icon} {icon}', blink_charging_icon: True}` | Options for charging state display.                                         |
| `status_thresholds`     | dict    | `{critical: 10, low: 25, medium: 75, high: 95, full: 100}` | Thresholds for different battery statuses.                                  |
| `status_icons`          | dict    | `{icon_charging: '\uf0e7', icon_critical: '\uf244', icon_low: '\uf243', icon_medium: '\uf242', icon_high: '\uf241', icon_full: '\uf240'}` | Icons for different battery statuses.                                       |
| `callbacks`             | dict    | `{on_left: 'toggle_label', on_middle: 'do_nothing', on_right: 'do_nothing'}` | Callback functions for different mouse button actions.                      |


## Example Configuration
```yaml
battery:
  type: "yasb.battery.BatteryWidget"
  options:
    label: "<span>{icon}</span>{percent}%"
    label_alt: "{icon} {percent}% | time: {time_remaining}"
    charging_options:
      icon_format: "{charging_icon}"
```

# Battery Widget Configuration

## Options

### `label`
- **Type:** `string`
- **Default:** `{icon}`
- **Description:** The primary label format for the battery widget. It can include placeholders like `{icon}` to dynamically display the battery icon.

### `label_alt`
- **Type:** `string`
- **Default:** `{percent}% | remaining: {time_remaining}`
- **Description:** The alternative label format for the battery widget. It can include placeholders like `{percent}` and `{time_remaining}` to dynamically display the battery percentage and remaining time.

### `update_interval`
- **Type:** `integer`
- **Default:** `5000`
- **Description:** The interval in milliseconds to update the widget.

### `time_remaining_natural`
- **Type:** `boolean`
- **Default:** `False`
- **Description:** Whether to display the remaining time in a natural format.

### `charging_options`
- **Type:** `dict`
- **Default:** `{icon_format: '{charging_icon} {icon}', blink_charging_icon: True}`
- **Description:** Options for displaying the charging state. The `icon_format` can include the `{charging_icon}` and `{icon}` placeholders to dynamically display the charging icon and battery icon. The `blink_charging_icon` option determines whether the charging icon should blink.

### `status_thresholds`
- **Type:** `dict`
- **Default:** `{critical: 10, low: 25, medium: 75, high: 95, full: 100}`
- **Description:** Thresholds for different battery statuses. These thresholds define the battery percentage ranges for critical, low, medium, high, and full statuses.

### `status_icons`
- **Type:** `dict`
- **Default:** `{icon_charging: '\uf0e7', icon_critical: '\uf244', icon_low: '\uf243', icon_medium: '\uf242', icon_high: '\uf241', icon_full: '\uf240'}`
- **Description:** Icons for different battery statuses. Each status (charging, critical, low, medium, high, full) has a corresponding icon.

### `callbacks`
- **Type:** `dict`
- **Default:** `{on_left: 'toggle_label', on_middle: 'do_nothing', on_right: 'do_nothing'}`
- **Description:** Callback functions for different mouse button actions. The `on_left`, `on_middle`, and `on_right` options define the functions to be called when the left, middle, or right mouse buttons are clicked on the widget.
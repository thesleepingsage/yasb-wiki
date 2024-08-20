# Komorebi Workspaces Widget
| Option                     | Type    | Default                  | Description                                                                 |
|----------------------------|---------|--------------------------|-----------------------------------------------------------------------------|
| `label_offline`          | string  | `'Komorebi Offline'`     | The label to display when Komorebi is offline.                              |
| `label_workspace_btn`    | string  | `'{index}'`              | The format string for workspace buttons.                                    |
| `label_workspace_active_btn` | string | `'{index}'`              | The format string for the active workspace button.                          |
| `label_default_name`       | string  | `''`                     | The default name for workspaces.                                            |
| `hide_if_offline`       | boolean | `false`         | Whether to hide the widget if Komorebi is offline.                          |
| `label_zero_index`        | boolean | `false`    | Whether to use zero-based indexing for workspace labels.                    |
| `hide_empty_workspaces`  | boolean | `false`      | Whether to hide empty workspaces.                                           |

## Example Configuration

```yaml
komorebi_workspaces:
  type: "komorebi.workspaces.WorkspaceWidget"
  options:
    label_offline: "Komorebi Offline"
    label_workspace_btn: "\udb81\udc3d"
    label_workspace_active_btn: "\udb81\udc3e"
    label_default_name: ""
    label_zero_index: false
    hide_empty_workspaces: false
    hide_if_offline: false
```

## Description of Options
- **label_offline:** The label to display when Komorebi is offline.
- **label_workspace_btn:** The format string for workspace buttons, can be icon, {name} or {index}.
- **label_workspace_active_btn:** The format string for the active workspace button, can be icon, {name} or {index}.
- **label_default_name:** The default name for workspaces.
- **hide_if_offline:** Whether to hide the widget if Komorebi is offline.
- **label_zero_index:** Whether to use zero-based indexing for workspace labels.
- **hide_empty_workspaces:** Whether to hide empty workspaces.
# Applications Widget Options
| Option     | Type   | Default | Description                                                                 |
|------------|--------|---------|-----------------------------------------------------------------------------|
| `label`   | string | {data}    | The label for the applications widget.                                      |
| `class_name` | string | `""` | The CSS class name for styling the widget. Optional.                        |
| `app_list`  | list   | `[]`| Application list with command. |

## Example Configuration

```yaml
apps:
  type: "yasb.applications.ApplicationsWidget"
  options:
    label: "{data}"
    app_list:
      - {icon: "\uf0a2", launch: "notification_center"}
      - {icon: "\ueb51", launch: "quick_settings"}
      - {icon: "\uf422", launch: "search"}
      - {icon: "\uf489", launch: "wt"}
      - {icon: "\udb82\ude1e", launch: "C:\\Users\\Username\\AppData\\Local\\Programs\\Microsoft VS Code\\Code.exe"}
```

## Description of Options
- **label:** The label for the applications widget.
- **class_name:** The CSS class name for styling the widget. Optional.
- **app_list:** A list of applications to display. Each application should be a dictionary with [`icon`] and [`launch`] keys. As launch you can call `quick_settings`, `notification_center`, `search`, `widget`, `launcher (launcher will trigger ALT+A)`.
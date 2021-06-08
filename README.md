# Buoys
`buoy` object lists the details of a buoy. This includes when it was launched, retired and when it most recently had wave data added.

### Attributes
| Tag | Type | Description |
| ------------- | ------------- | ----- |
| `buoy_id` | `string` | Unique identifier for this buoy **Required** |
| `label` | `string` | Label for internal use I.e. 'PortHeadland #32' **Required** |
| `web_display_label` | `string` | Label for pretty title for the buoy I.e. 'Port Headland Deap Sea' **Required** |
| `type` | `string` | Buoy manufacturer **Required** |
| `enabled` | `integer` | `0` not visible, `1` visible, `2` map only, `3` chart only  **Required** |
| `order` | `integer` | Order in list on website **Required** |
| `data` | `string` | Additional data |
| `start_date` |  `unix timestamp` | Deployed date **Required** |
| `end_date` |  `unix timestamp` | Completion date if ended |
| `first_updated` | `unix timestamp` | Filename for first CSV written |
| `last_updated` | `unix timestamp` | Filename for most recently written CSV |
| `drifting` | `boolean` | If the buoy is drifiting **Required** |

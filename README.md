# Buoys
`buoy` object lists the details of a buoy. This includes when it was launched, retired and when it most recently had wave data added.

### Attributes
| Tag | Type | Description |
| ------------- | ------------- | ----- |
| `buoy_id` | `integer` | Unique identifier for this buoy **(Required)** |
| `label` | `string` | Label/Slug for internal use I.e. 'PortHeadland'. No spaces. **(Required)** |
| `web_display_label` | `string` | Label for pretty title for the buoy I.e. 'Port Headland Deap Sea' **(Required)** |
| `type` | `string` | Buoy manufacturer |
| `enabled` | `integer` | `0` not visible, `1` visible, `2` map only, `3` chart only  **(Required)** |
| `order` | `integer` | Order of appearance in buoys list on website **(Required)** |
| `data` | `string` | Area to place additional data for later reference or use |
| `start_date` |  `timestamp` | Date buoy was deployed **(Required)** |
| `end_date` |  `timestamp` | Date buoy was retired |
| `first_updated` | `timestamp` | Date first wave data was written **(Required)** |
| `last_updated` | `timestamp` | Date most recent update was made **(Required)** |
| `drifting` | `boolean` | If the buoy is drifiting **(Required)** |
| `latitude` | `float` | Launch latitude |
| `longitude` | `float` | Launch longitude |

# Waves
`wave` object lists a specific wave event recording.

### Attributes
| Tag | Type | Description |
| ------------- | ------------- | ----- |
| `wave_id` | `integer` | Unique id for this wave event **(Required)** | 
| `buoy_id` | `integer` | `buoy_id` this event data is linked to **(Required)** | 
| `timestamp` | `timestamp` | Unix timestamp UTC for this wave event **(Required)** | 
| `timestamp_reference` | `string` | Human readable UTC datetime in the industry standard format `dd-M-yyyy hh:mm:ss` for example `05-Dec-2001 22:11:40` **(Required)** | 
| `hsig` | `float` | Significant Wave Height (metres) |
| `tp` | `float` | Peak Wave Period (s) |
| `tm` | `float` | Mean Wave Period (s) |
| `dp` | `float` | Peak Wave Direction (deg) |
| `dpspr` | `float` | Peak Wave Directional Spreading (deg) |
| `dm` | `float` | Mean Wave Direction (deg) |
| `dmspr` | `float` | Mean Wave Directional Spreading (deg) |
| `qf_waves` | `float` | Wave data quality |
| `sst` | `float` | Sea Surface Temperature (degC) |
| `qf_sst` | `float` | Sea Surface Temperature data quality |
| `bottom temp` | `float` | Sea Bottom Temperature (degC) |
| `qf_bott_temp` | `float` | Sea Bottom Temperature quality |
| `windspeed` | `float` | Wind Speed (m/s) |
| `winddirec` | `float` | Wind Direction (deg) |
| `currmentmag` | `float` | Current Mag (m/s) |
| `currentdir` | `float` | Current Direction (deg) |
| `latitude` | `float` | Current latitude |
| `longitude` | `float` | Current longitude |

# Occasions, a FiestaBoard plugin

Schedule a custom message for a specific date, and see it on that day. No calendar needed, all details are stored in plugin settings.

## Configure

| Setting | Notes |
|---|---|
| Occasions | One row per message: date (`YYYY-MM-DD`), message, optional colors. Use `|` for line breaks. Past dates are ignored. |
| Timezone | Defaults to America/Chicago. |
| Upcoming Window | How far ahead `occasions.upcoming` looks. Default 30 days. |
| Take Over the Board | Takes over on that day. Off by default. |
| Takeover Priority | Higher number wins. Default 60. |

### Page recipes

Today's message, or nothing:

```text
{{= IFERROR(occasions.message, "") }}
```

Supports Vestaboard and Vestaboard Note

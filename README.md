# Helper Plugin

*anomaly.plugin.helper*

#### A plugin that provides numerous helpful PHP functions.

The Helper Plugin extends the Streams Platform with additional utility functions available throughout your application.

## Features

- Utility helper functions
- Template helper functions
- Array manipulation helpers
- String manipulation helpers
- URL generation helpers
- Date/time helpers
- Form helpers
- Additional Twig functions

## Usage

### String Helpers

```twig
{# Truncate string #}
{{ str_truncate(text, 100) }}

{# Slug generation #}
{{ str_slug('My Article Title') }}

{# Limit words #}
{{ str_limit_words(description, 50) }}

{# Parse markdown #}
{{ parse_markdown(content)|raw }}
```

### Array Helpers

```twig
{# Get array value with default #}
{{ array_get(data, 'key.nested', 'default') }}

{# Check if array has key #}
{% if array_has(data, 'key') %}
    ...
{% endif %}

{# Get first/last element #}
{{ array_first(items) }}
{{ array_last(items) }}
```

### URL Helpers

```twig
{# Generate URLs #}
{{ url_to('path/to/page') }}
{{ url_secure('path') }}

{# Check current URL #}
{% if url_is('admin/*') %}
    <p>Admin section</p>
{% endif %}
```

### Date Helpers

```twig
{# Format dates #}
{{ format_date(date, 'F j, Y') }}

{# Relative time #}
{{ time_ago(created_at) }}

{# Human readable diff #}
{{ human_time(minutes) }}
```

## Requirements

- Streams Platform ^1.10
- PyroCMS 3.10+

## License

The Helper Plugin is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT).

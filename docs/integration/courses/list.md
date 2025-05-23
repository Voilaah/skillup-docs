# Courses list

<Badge type="warning">Page is Work in Progress</Badge>

SkillUp can import all or part of your courses directly from your platform.

::: info INFO
This API allows SkillUp to display the list of your courses and their respective course preview page giving minimum information to the students before enrolling.
:::

## API requirements

Your platform needs to provide the following API to retrieve your courses list.

<Badge>GET</Badge> `https://your-external-platform.com/api/v1/courses`

The API needs to respond to the following specifications:

**Query parameters**
| Field | Type | Default | Description |
|---|---|---|---|
| page | number | 1 | Page number to retrieve |
| per_page | number | 10 | Number of courses to retrieve |

<br/>
**API returns**

```jsonc
{
    "total": 52,
    "per_page": 10,
    "current_page": 2,
    "last_page": 5,
    "prev_page_url": "https://your-external-platform.com/api/v1/courses?page=1",
    "next_page_url": "https://your-external-platform.com/api/v1/courses?page=3",
    "data" : [
        {
            "id": 1,
            "code": "001",
            "title": "A course title",
            "thumbnail": "https://your-external-platform.com/storage/app/medias/courses/thumbnail/181120100340-hairdresser-3572053_1280.jpg",
            "introduction": "Dolor commodo aliquip veniam labore amet elit. Laboris culpa quis id consequat voluptate officia tempor consectetur aliquip duis laborum occaecat.",
            "description": "Dolor commodo aliquip veniam labore amet elit. Laboris culpa quis id consequat voluptate officia tempor consectetur aliquip duis laborum occaecat.

            Dolor commodo aliquip veniam labore amet elit. Laboris culpa quis id consequat voluptate officia tempor consectetur aliquip duis laborum occaecat",
            "objectives": "Dolor commodo aliquip veniam labore amet elit. Laboris culpa quis id consequat voluptate officia tempor consectetur aliquip duis laborum occaecat.",
            "outcomes": "Dolor commodo aliquip veniam labore amet elit. Laboris culpa quis id consequat voluptate officia tempor consectetur aliquip duis laborum occaecat.",
            "skills": "Dolor commodo aliquip veniam labore amet elit. Laboris culpa quis id consequat voluptate officia tempor consectetur aliquip duis laborum occaecat.",
            "inclusion": "Dolor commodo aliquip veniam labore amet elit. Laboris culpa quis id consequat voluptate officia tempor consectetur aliquip duis laborum occaecat.",
            "url": "https://your-external-platform.com/courses/123456",
            "meta" : {
                "duration": 150,
                "organization": "Organization name",
                "level": "beginner",
                "category": "category 1",
                "is_coming_soon": false,
                "is_published": true,
                "has_certificate": true,
                "is_free": true,
                "price": null,
                "locale": "en",
                "last_updated_at" : "2025-05-21 16:55:00"
            }
        },
    ]
}
```

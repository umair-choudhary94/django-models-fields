

## 🧱 Django Model Fields (Cheat Sheet)

| **Field** | **Description** |
|-----------|-----------------|
| `CharField` | Text field for small to medium strings (`max_length` required). |
| `TextField` | For large blocks of text (no `max_length` required). |
| `IntegerField` | Stores integer values. |
| `FloatField` | Stores floating-point numbers. |
| `DecimalField` | Stores fixed-point decimal numbers (useful for money). Requires `max_digits` and `decimal_places`. |
| `BooleanField` | True/False field (checkbox). |
| `NullBooleanField` | True/False/Unknown (use `BooleanField(null=True)` instead in Django 3.1+). |
| `DateField` | Stores date (YYYY-MM-DD). Use `auto_now` or `auto_now_add`. |
| `TimeField` | Stores time (HH:MM[:ss[.uuuuuu]]). |
| `DateTimeField` | Stores both date and time. |
| `EmailField` | Stores and validates email addresses. |
| `URLField` | Stores and validates URLs. |
| `SlugField` | Stores short labels (usually for URLs, no spaces). |
| `FileField` | Upload and store files (needs `MEDIA_ROOT` and `MEDIA_URL`). |
| `ImageField` | Upload and store images (requires Pillow library). |
| `UUIDField` | Stores universally unique identifiers (UUIDs). |
| `BinaryField` | Stores raw binary data. |
| `JSONField` | Stores JSON data (PostgreSQL 9.2+, built-in since Django 3.1). |
| `BigIntegerField` | Like `IntegerField`, but supports larger numbers. |
| `PositiveIntegerField` | Only allows positive integers (deprecated – use `PositiveBigIntegerField` in newer versions). |
| `PositiveSmallIntegerField` | Smaller positive integers. |
| `SmallIntegerField` | Stores small integers (less memory). |
| `DurationField` | Stores time durations (`timedelta` objects). |

---

## 🔁 Relationship Fields

| **Field** | **Description** |
|-----------|-----------------|
| `ForeignKey` | One-to-many relationship (links to another model). |
| `OneToOneField` | One-to-one relationship. |
| `ManyToManyField` | Many-to-many relationship between models. |

---

## ⚙️ Common Field Options (Arguments)

You can pass these as parameters to most fields:

| **Option** | **Description** |
|------------|------------------|
| `null=True` | Allows `NULL` in the database. |
| `blank=True` | Field is optional in forms. |
| `default=value` | Sets a default value. |
| `choices=[(v1, label1), (v2, label2)]` | Defines fixed choices. |
| `unique=True` | Field must be unique. |
| `verbose_name='Custom Name'` | Human-readable name. |
| `help_text='Helpful hint.'` | Shown in forms/admin. |

---

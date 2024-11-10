# Styling

## Prefer tailwind

I have so far found tailwind to be the most concise and easiest way to style components in a reflex app.  For instance the following may be comparable:


using tailwind in reflex:

```python
rx.box(
    ...,
    class_name="max-w-md w-full space-y-8 bg-white p-8 rounded-xl shadow-lg",
)
```
while equavalently doing this using the reflex common props would be something like:

```python
rx.box(
    ...,
    background_color="white",
    width="100%",
    max_width="28em",
    padding="2rem",
    border_radius="1rem",
    box_shadow="0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1)",
)
```


## Tailwind enabling

So far I have not found the tailwind extending/styling to work, for instance in `saas_config.py` trying to make all the indigo colors green:

```python

tailwind_config = {
    "theme": {
        "extend": {
            "colors": {
                "indigo": {
                    "1": "var(--green-1)",
                    "2": "var(--green-2)",
                    "3": "var(--green-3)",
                    "4": "var(--green-4)",
                    "5": "var(--green-5)",
                    "6": "var(--green-6)",
                    "7": "var(--green-7)",
                    "8": "var(--green-8)",
                    "9": "var(--green-9)",
                    "10": "var(--green-10)",
                    "11": "var(--green-11)",
                    "12": "var(--green-12)",
                    "a1": "var(--green-a1)",
                    "a2": "var(--green-a2)",
                    "a3": "var(--green-a3)",
                    "a4": "var(--green-a4)",
                    "a5": "var(--green-a5)",
                    "a6": "var(--green-a6)",
                    "a7": "var(--green-a7)",
                    "a8": "var(--green-a8)",
                    "a9": "var(--green-a9)",
                    "a10": "var(--green-a10)",
                    "a11": "var(--green-a11)",
                    "a12": "var(--green-a12)",
                },
            },
        }
    },
    "plugins": [
        "@tailwindcss/typography",
    ],
}
```


# components

Some helpful links
- https://reflex.dev/docs/styling/common-props/
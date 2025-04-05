# 🔥 Flint

**Flint** is a lightweight, opinionated Python library for writing safe, clean, and high-performance PySpark code. Just like flint sparks fire, this library helps you ignite better Spark pipelines—with guardrails, best practices, and developer-friendly patterns.

---

## ✨ Why Flint?

Working with PySpark is powerful—but it's easy to fall into traps like:
- Inefficient joins and UDFs
- Excessive .collect() or .toPandas()
- Inconsistent I/O and schema handling
- Poorly structured streaming jobs

Flint helps by providing:
- 🔄 **Composable transformations** via .transform() (like Pandas' .pipe())
- 🧠 **Safe helpers** for joins, I/O, schema validation, and performance tuning
- 🧪 **Testable building blocks** for batch and streaming jobs
- 🧰 **Minimal APIs** you can adopt gradually—no lock-in

---

## 📦 Example (Coming Soon)

```python
from flint.transforms import clean_column_names, safe_broadcast_join

df = (
    spark.read.csv("data.csv", header=True)
    .transform(clean_column_names)
    .transform(safe_broadcast_join, lookup_df, on="user_id")
)
```

## 📍 Status

Flint is currently in early development.

If you're interested in contributing ideas or want to follow progress, feel free to ⭐️ star this repo and watch for updates.

## 🛠️ Planned Modules - Might change

* `flint.transforms` – clean, testable DataFrame helpers
* `flint.streaming` – safe wrappers for watermarking, state, event-time
* `flint.io` – schema-aware reads & writes
* `flint.utils` – hashing, UUIDs, logging, partitioning
* `flint.decorators` – logging, performance tracing, and guards

## 💡 Philosophy

Flint is:
* 🧼 **Clean** – encourages idiomatic, readable Spark pipelines
* 🧱 **Compositional** – each part is modular and testable
* 🧯 **Safe** – helps teams avoid costly production mistakes
* 👥 **Team-friendly** – makes onboarding and collaboration easier

## 🔗 License

MIT – Open and free to use.

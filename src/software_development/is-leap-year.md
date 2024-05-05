# Is Leap Year

## Kata

**Rust**

```rust
{{#rustdoc_include is-leap-year/src/main.rs:2:7}}
```

### Notes

The rules for determining if a year is a **leap year**:

- Years divisible by 4 are leap years,
- but years divisible by 100 are **not** leap years,
- but years divisible by 400 are leap years.

## Chrestomathy

**SQL**

```sql
select
  year,
  CASE
    WHEN year%400 = 0 THEN true
    WHEN year%100 = 0 THEN false
    WHEN year%4 = 0 THEN true
    ELSE false
  END as is_leap
from years
order by year;
```

---

## Sources

- [Codewars](https://www.codewars.com/kata/526c7363236867513f0005ca)

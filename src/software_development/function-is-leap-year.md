# Is Leap Year

## Notes

The rules for determining if a year is a **leap year**:

- Years divisible by 4 are leap years,
- but years divisible by 100 are **not** leap years,
- but years divisible by 400 are leap years.

## Kata

**Rust**

```rust
fn is_leap_year(year: i32) -> bool {
    match (year % 400, year % 100, year % 4) {
        (0, _, _) => true,
        (_, 0, _) => false,
        (_, _, 0) => true,
        _ => false,
    }
}
```

### Test cases

```rust,no_run,ignore
#[cfg(test)]
mod sample_tests {
    use super::is_leap_year;

    fn do_test(year: i32, expected: bool) {
        let actual = is_leap_year(year);
        assert_eq!(actual, expected, "\nYour result (left) does not match the expected output (right) for the year {year:?}");
    }

    #[test]
    fn year_2020_is_a_leap_year() {
        do_test(2020, true);
    }

    #[test]
    fn year_2000_is_a_leap_year() {
        do_test(2000, true);
    }

    #[test]
    fn year_2015_is_not_a_leap_year() {
        do_test(2015, false);
    }

    #[test]
    fn year_2100_is_not_a_leap_year() {
        do_test(2100, false);
    }
}
```

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

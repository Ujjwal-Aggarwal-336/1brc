# 1BRC

Barebones setup for the One Billion Row Challenge: compute min/mean/max temperature per weather station from a file of 1B rows (`station;temp`).

## Layout

- `src/main/java/dev/morling/onebrc/CalculateAverage_baseline.java` — reference solution
- `src/main/java/dev/morling/onebrc/CreateMeasurements*.java` — generate `measurements.txt`
- `calculate_average_*.sh` / `prepare_baseline.sh` — run / prepare a solution
- `create_measurements*.sh` — measurement generators
- `test.sh`, `test_all.sh` — check output against `src/test/resources/samples`

## Usage

```sh
./mvnw clean verify
./create_measurements.sh 1000000000   # writes measurements.txt
./calculate_average_baseline.sh
./test.sh baseline
```

Requires Java 21+.

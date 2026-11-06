# SAST for Minecraft Mods

Static analysis tool for Java/JVM bytecode scanning and heuristic threat assessment

## Dependencies

- [`cfr`](https://github.com/leibnitz27/cfr/releases/download/0.152/cfr-0.152.jar)
- `ripgrep`
- `grep`

## Synopsis

`./main.sh [PATH]`
  - `[PATH]`:
    The directory to scan for JARs to scan,
    Optional—if not provided will scan the current working directory CWD.

## Sample Output

For each JAR file analyzed, mod-sast generates a detailed report:

```txt
Analyzing "/path/to/file.jar" @ "2024-01-15 14:30:22"...

JAR references operating system & hardware identifiers 3 times.
java.time.ZoneId
oshi.hardware.HardwareAbstractionLayer
System.getProperty('os.name')

Points from OSHI: 25/85

[Additional category scores...]

Visible potential invasiveness: 142/525
Visible potential for destruction: 87/510
Likelihood of intent masking: 45/300
```

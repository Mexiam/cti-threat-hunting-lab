# Methodology

The project follows the following methodology:

1. Identify a real-world cyber campaign from public sources.
2. Extract the relevant attacker behaviors.
3. Map the behaviors to MITRE ATT&CK techniques.
4. Determine which behaviors can be safely reproduced in the laboratory.
5. Generate the corresponding activity in the isolated environment.
6. Collect the resulting telemetry.
7. Develop or adapt detection rules.
8. Test the detections.
9. Perform threat hunting based on the collected telemetry.
10. Measure detection coverage and document limitations.

## Workflow

```text
Real-world campaign
        |
        v
   CTI analysis
        |
        v
MITRE ATT&CK mapping
        |
        v
Controlled simulation
        |
        v
   Log collection
        |
        v
Detection engineering
        |
        v
 Threat Hunting
        |
        v
Detection evaluation
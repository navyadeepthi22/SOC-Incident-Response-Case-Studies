# Potential Data Exfiltration via External Service (Zoom)

## Incident Type
Suspected Data Exfiltration

## Alert Description
The alert was triggered when more than 5 GB of data was sent from an internal host to an external destination within a single day.

## Affected Assets
- Source IP: 192.168.45.66
- Host Location: UK04 / Meeting Room
- Destination Domain: *.zoom.us

## Network Context
The affected host is located in a meeting room network segment commonly used for video conferencing.

## Initial Analyst Assessment
Zoom is a trusted service and known for high data usage due to video and screen sharing. Suspicion level was assessed as medium.

## Evidence Observed
- Outbound data: 5.8 GB
- Inbound data: 5.2 GB
- Bidirectional traffic
- Destination domain belongs to Zoom

## MITRE ATT&CK Mapping
- Tactic: Exfiltration
- Technique: Exfiltration Over Web Services (T1567)

## Decision
False Positive

## Justification
High data transfer aligns with expected Zoom usage patterns. No indicators of malicious activity were observed.

## Recommended Actions
- Close alert as false positive
- Whitelist trusted collaboration tools
- Continue monitoring for unusual destinations
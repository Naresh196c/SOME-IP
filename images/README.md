# Assignment 2 – Wireshark Evidence

These screenshots were shared during the Assignment 2 Wireshark analysis.

| File | Evidence shown |
|---|---|
| `01-wireshark-service-discovery-packet-list.png` | SOME/IP Service Discovery traffic on loopback |
| `02-wireshark-both-services-offered.png` | One SD message containing OfferService entries for ClimateService (`0x2234`) and VehicleSpeedService (`0x1234`) |
| `03-wireshark-offer-service-details.png` | Expanded OfferService entries, including service and instance IDs |
| `04-wireshark-service-endpoint-options.png` | UDP endpoint options: ClimateService at `127.0.0.1:3001` and VehicleSpeedService at `127.0.0.1:3000` |
| `05-wireshark-get-vehicle-state-response.png` | `GetVehicleState` response; Service ID `0x1234`, Method ID `0x0002`, payload `01` (MOVING) |
| `06-wireshark-get-speed-request.png` | `GetSpeed` request; Service ID `0x1234`, Method ID `0x0001`, Session ID `0x018f` |
| `07-wireshark-get-speed-response.png` | Matching `GetSpeed` response; same Session ID `0x018f`, payload `0046` (70 km/h) |

## Evidence limitations

These images document the packets actually inspected. They do not provide screenshot evidence for every Assignment 2 task. In particular, ClimateService method exchanges and event notifications were not independently identified in these screenshots. The full packet capture is stored separately at `captures/assignment2-multi-ecu.pcapng`.

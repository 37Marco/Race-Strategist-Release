# Race Strategist

Race Strategist is a local-first live pit-stop outcome simulator for iRacing.
It reads the pit services currently selected in iRacing and estimates what
happens if you pit now.

[Download the latest Windows release](https://github.com/37Marco/Race-Strategist-Release/releases/latest)

> Race Strategist is currently an MVP. Predictions are estimates and should
> support — not replace — the driver's own judgement.

## Current features

- Live PIT NOW rejoin prediction
- Estimated service time and total pit loss
- Projected class position and nearest cars ahead and behind
- Signed gaps, recent observed pace and immediate traffic risk
- Selected fuel, tyres, tear-off and Fast Repair detection
- Track-and-car-specific calibration from valid local pit stops
- Multiclass identification
- Explicit confidence, penalty and mandatory-repair uncertainty
- Local telemetry processing without an account or cloud connection

## Requirements

- Windows 10 or Windows 11, 64-bit
- iRacing

Python and Node.js are not required for the packaged application.

## Installation

1. Open the [latest release](https://github.com/37Marco/Race-Strategist-Release/releases/latest).
2. Download **Race-Strategist-Setup-0.1.0.exe**.
3. Run the installer and start Race Strategist.
4. Start or join an active iRacing session.

The application is not currently code-signed. Windows SmartScreen may therefore
show a warning for the downloaded installer.

## Calibration

Race Strategist learns pit-loss data locally for each track-and-car
combination. A new combination needs one valid completed pit stop before a
calibrated rejoin prediction becomes available. Additional valid stops improve
the local baseline.

## Current MVP boundaries

- Evaluates only the result of pitting now
- Does not decide whether you should pit
- Does not recommend a fuel quantity
- Does not calculate a full-race strategy
- Does not predict future opponent pit stops
- Keeps uncertain or missing information visibly unavailable

## Privacy

Race telemetry, observations and predictions remain on the local Windows
computer. No account, cloud telemetry or permanent internet connection is
required during a race.

## Verify the download

Every release publishes a SHA256 checksum. Check the downloaded installer in
PowerShell:

    Get-FileHash ".\Race-Strategist-Setup-0.1.0.exe" -Algorithm SHA256

Compare the result with the checksum shown in the matching GitHub release.

## Project

The application source code is maintained in a private repository. This public
repository contains release information and downloadable installers only.

Race Strategist is an independent project and is not affiliated with
iRacing.com.

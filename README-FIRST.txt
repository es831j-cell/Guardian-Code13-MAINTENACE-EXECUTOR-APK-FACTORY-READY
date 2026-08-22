LUMI GUARDIAN CODE 13 — MAINTENANCE EXECUTOR

Purpose
- Upgrade the installed Guardian from code 12 to code 13 without rebuilding Lumi.
- Satisfy Lumi Code 320's GUARDIAN_UPDATE_REQUIRED gate.
- Add the bounded runtime repair executor used by Lumi's maintenance bridge.

Expected identity
- package: com.distressedelk.lumi.guardian
- versionCode: 13
- versionName: 2.2-maintenance-executor

Runtime repair allow-list
- speech_rebuild
- bridge_reinitialize
- fast_brain_recover
- mobius_recover
- runtime_health_recheck

Safety boundary
- No shell or arbitrary file writes.
- No unsigned core replacement.
- Core Lumi code changes still require a signed verified APK.

Build/install
1. Build this ZIP in APK Factory.
2. Install it OVER the existing Lumi Guardian app. Do not uninstall Guardian first.
3. Open Lumi Code 320 and run/check the maintenance bridge.
4. Diagnostics should report Guardian version 13 and BRIDGE_CONNECTED.

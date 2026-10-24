Iontrace: Physics-Informed Object-Relational Schema

> Functional MVP Prototype: Built for rapid algorithm validation, multi-vendor binary file parsing (.mpr, .nda, .res), and electrochemical physics constraint enforcement.

---

> Quick Test Instructions (10-Second Validation)

Reviewers can test the prototype in two ways:

> Option A: One-Click Instant Run (Fastest)
1. Launch the live prototype: https://iontrace-mvp-awehfh6b3gludikjdcvrnr.streamlit.app/
2. Select " Instant Demo (Pre-loaded CALCE Run)" in the sidebar to execute the pipeline immediately.

> Option B: Test Manual Drag-and-Drop
1. Generate the test dataset on your desktop using your terminal:

   Windows PowerShell:
   ```powershell
   @'
   Time_s,Voltage_V,Capacity_mAh,Step_Index
   0,3.00,0,1
   300,3.40,250,1
   600,3.75,500,1
   900,3.95,750,1
   1200,4.10,1000,1
   1500,4.20,1200,1
   '@ | Out-File -FilePath "$([Environment]::GetFolderPath('Desktop'))\calce_test_run.csv" -Encoding utf8; Write-Host "Success! calce_test_run.csv created on Desktop!" -ForegroundColor Green

   macOS & Linux Terminal (Bash / Zsh):
   cat << 'EOF' > ~/Desktop/calce_test_run.csv
Time_s,Voltage_V,Capacity_mAh,Step_Index
0,3.00,0,1
300,3.40,250,1
600,3.75,500,1
900,3.95,750,1
1200,4.10,1000,1
1500,4.20,1200,1
EOF
echo "Success! calce_test_run.csv created on Desktop!"

> Confirm that calce_test_run.csv was created on your Desktop.
> Open the live prototype: https://iontrace-mvp-awehfh6b3gludikjdcvrnr.streamlit.app/
> Drag calce_test_run.csv from your Desktop straight into the 1. Ingest Hardware Data upload box in the left sidebar.
> The dashboard will process the file instantly, update the metrics (Max Voltage: 4.200 V, Capacity: 1200.00 mAh), and render the dark-mode Plotly curve live on screen.

----

Architecture Overview:
> Ingestion Layer: Edge daemon polling & zero-touch binary parsing (.mpr, .nda, .res).
> Translation Engine: Multi-vendor schema normalization into unified physics tensors.
> Physics Guardrails: Deterministic thermodynamic/kinetic boundary checks preventing AI hallucinations.

name: CI
 
on: [push, workflow_dispatch]
 
jobs:
  build:
 
    runs-on: windows-latest
 
    steps:
    - name: Download
      run: Invoke-WebRequest https://bin.equinox.io/c/4VmDzA7iaHb/ngrok-stable-windows-amd64.zip -OutFile ngrok.zip
    - name: Extract
      run: Expand-Archive ngrok.zip

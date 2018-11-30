FROM microsoft/windowsservercore:1803

RUN powershell.exe -Command \
    $ErrorActionPreference = 'Stop'; \
    $ProgressPreference = 'SilentlyContinue'; \
    $url = 'https://download.sysinternals.com/files/SysinternalsSuite.zip'; \
    Invoke-WebRequest $url -OutFile suite.zip; \
    Expand-Archive suite.zip 'C:\sysinternals'; \
    rm suite.zip

WORKDIR C:\\sysinternals


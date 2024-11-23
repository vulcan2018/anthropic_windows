# anthropic_windows
Steps to get Computer Use on Windows with Claude
Download docker
open a cmd terminal and type
docker pull ghcr.io/anthropics/anthropic-quickstarts:computer-use-demo-latest
mkdir c:\anthropic         #or similar
docker run ^
    -e ANTHROPIC_API_KEY=%ANTHROPIC_API_KEY% ^
    -v c:\anthropic:/home/computeruse/.anthropic ^
    -p 5900:5900 ^
    -p 8501:8501 ^
    -p 6080:6080 ^
    -p 8080:8080 ^
    -it ghcr.io/anthropics/anthropic-quickstarts:computer-use-demo-latest

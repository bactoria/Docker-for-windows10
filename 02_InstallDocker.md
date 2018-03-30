


#도커 설치 (Windows10)

> 도커 종류 2개가 있다.
> `Docker Toolbox` 와 `Docker-for-windows(+hyper-v)`
> `Docker-for-windows`는 윈도우10 64bit를 지원하기때문에
> 하위버전은 Docker Toolbox를 써야한다.

[Docker-for-windows 홈페이지에서 설치](https://docs.docker.com/docker-for-windows/install/) 할수도 있지만, chocolatey로 설치할래~~

<BR/>


<BR/>

**관리자모드로 cmd 실행**

![](assets/markdown-img-paste-20180327173748692.png)

<BR/>

**chocolatey 설치**

```
@"%SystemRoot%\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -InputFormat None -ExecutionPolicy Bypass -Command "iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))" && SET "PATH=%PATH%;%ALLUSERSPROFILE%\chocolatey\bin"
```

![](assets/markdown-img-paste-20180327151717248.png)

<br/>


**docker 설치**
```
choco install docker-for-windows --ignore-checksums -y
```

<br/>

**환경변수 추가**

```
setx path=%path%;C:\Program Files\Docker\Docker\resources\bin
```

<br/>

**cmd 껐다 키자~**

<br/>

**docker 버전확인** **`docker version`**

```
C:\Users\bactoria>docker version
Client:
 Version:       18.03.0-ce
 API version:   1.37
 Go version:    go1.9.4
 Git commit:    0520e24
 Built: Wed Mar 21 23:06:28 2018
 OS/Arch:       windows/amd64
 Experimental:  false
 Orchestrator:  swarm

Server:
 Engine:
  Version:      18.03.0-ce
  API version:  1.37 (minimum version 1.12)
  Go version:   go1.9.4
  Git commit:   0520e24
  Built:        Wed Mar 21 23:14:32 2018
  OS/Arch:      linux/amd64
  Experimental: false

C:\Users\bactoria>
```

<br/>

**Docker for Windows.exe 실행하기**

`docker version` 쳤을 때 위와 다르게 나온다면

도커 켜져있는지 확인.

![](assets/markdown-img-paste-20180327232938336.png)


<br/>

**Hyper-V 설정**
![](assets/markdown-img-paste-20180325135122737.png)

`Hyper-V` 가능하게 할거냐? 를 묻는다면

Ok 누르자.

( 누르면 재부팅된다. )

<br/>

-끝-

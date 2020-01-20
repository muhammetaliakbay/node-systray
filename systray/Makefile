.PHONY: all darwin linux windows clean

darwin:
	CGO_ENABLED=1 GOARCH=amd64 go build -o ./build/tray_darwin_amd64 -ldflags "-s -w" tray.go
	CGO_ENABLED=1 GOARCH=386 go build -o ./build/tray_darwin_386 -ldflags "-s -w" tray.go

linux:
	CGO_ENABLED=1 GOARCH=amd64 go build -o ./build/tray_linux_amd64 -ldflags "-s -w" tray.go
	CGO_ENABLED=1 GOARCH=386 go build -o ./build/tray_linux_386 -ldflags "-s -w" tray.go

windows:
	CGO_ENABLED=1 GOARCH=amd64 go build -o ./build/tray_windows_amd64.exe -ldflags "-s -w" tray.go
	CGO_ENABLED=1 GOARCH=386 go build -o ./build/tray_windows_386.exe -ldflags "-s -w" tray.go

clean:
	rm -rf ./build;
	mkdir -p ./build;

all: clean darwin linux windows
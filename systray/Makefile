.PHONY: all clean darwin linux windows

darwin:
	CGO_ENABLED=1 GOOS=darwin GOARCH=amd64 go build -o ./build/tray_darwin_amd64 -ldflags "-s -w" tray.go
	CGO_ENABLED=1 GOOS=darwin GOARCH=386 go build -o ./build/tray_darwin_i386 -ldflags "-s -w" tray.go

linux:
	CGO_ENABLED=1 GOOS=linux GOARCH=amd64 go build -o ./build/tray_linux_amd64 -ldflags "-s -w" tray.go
	CGO_ENABLED=1 GOOS=linux GOARCH=386 go build -o ./build/tray_linux_i386 -ldflags "-s -w" tray.go

windows:
	CGO_ENABLED=1 GOOS=windows GOARCH=amd64 go build -o ./build/tray_windows_amd64.exe -ldflags "-s -w" tray.go
	CGO_ENABLED=1 GOOS=windows GOARCH=386 go build -o ./build/tray_windows_i386.exe -ldflags "-s -w" tray.go

clean:
	rm -rf ./build;
	mkdir -p ./build;

all: clean windows linux darwin
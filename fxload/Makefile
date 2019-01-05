PREFIX=/usr/local
BINDIR=$(PREFIX)/bin
XCODEPROJ=fxload.xcodeproj
TARGET=build/Release/fxload
SRC=*[mh]
INSTALL=install

all: $(TARGET)

.PHONY: clean install
clean:
	rm -rf $(XCODEPROJ) build

install: $(TARGET)
	$(INSTALL) -d $(BINDIR)
	$(INSTALL) -c -m 755 $(TARGET) $(BINDIR)

$(TARGET): $(SRC) $(XCODEPROJ)
	xcodebuild -configuration Release

$(XCODEPROJ): project.yml
	@# brew install xcodegen
	xcodegen

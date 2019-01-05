XCODEPROJ=fxload.xcodeproj
TARGET=build/Release/fxload
SRC=*[mh]

all: $(TARGET)

.PHONY: clean install
clean:
	rm -rf $(XCODEPROJ) build

install: $(TARGET)
	cp $(TARGET) /usr/local/bin/fxload

$(TARGET): $(SRC) $(XCODEPROJ)
	xcodebuild -configuration Release

$(XCODEPROJ): project.yml
	@# brew install xcodegen
	xcodegen

all: build_xcode

clean: clean_builds

install: all
	sudo cp -R \
		build_xcode/build/Release/karabiner_observer.app \
		'/Library/Application Support/org.pqrs/Karabiner-Elements/Applications'
	sudo killall karabiner_observer

include ../../Makefile.rules

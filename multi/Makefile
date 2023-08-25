LIBS = $(shell find * -type d)
MODE = debug

.PHONY: all debug release clean $(LIBS) 

all: debug

debug: MODE = debug
debug: $(LIBS)

release: MODE = release
release: $(LIBS)

$(LIBS):
	echo building $@ as $(MODE) 
	@$(MAKE) -C $@ $(MODE)

clean:
	@for dir in $(LIBS); do \
		echo cleaning $$dir; \
		$(MAKE) -C $$dir clean; \
	done

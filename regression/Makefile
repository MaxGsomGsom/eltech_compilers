TESTS=test001 test002 test003 test004 test005 test006 test007 test008 test012 test013 test009 test010 test014 test015 test016 test017 test018 iftest test019 test020 test021 test022 test023 test011 test024 test025 test026

#Expressions:
#test001 test002 test003 test004 test005 test006 test007 test008 test012 test013

#If, while:
#test009 test010 test014 test015 test016 test017 test018 iftest

#For
#test019 test020 test021 test022

#Until
#test023

#Func
# test011 test024 test025 test026 

# Later:
# test027 test028 test029 test030

.PHONY: check $(TESTS)

check: $(TESTS)

$(TESTS): %: %.expr
#	../rc.native $< ; cat $@.input | ./$@ > $@.log ; diff $@.log orig/$@.log
	cat $@.input | ../rc.native -i $< > $@.log ; diff $@.log orig/$@.log
	cat $@.input | ../rc.native -s $< > $@.log ; diff $@.log orig/$@.log

clean:
	rm -f test*.log *.s *~ $(TESTS)

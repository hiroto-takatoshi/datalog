all:	succ.dl
	@echo
	@echo '*******'
	@echo Use succ implemented as a database table
	wc succ.dl
	tail -3 succ.dl
	cat even.dl
	@echo Run datalog
	cat succ.dl even.dl | time -p ../datalog -
	@echo
	@echo '*******'
	@echo Use succ implemented a primitive
	cat succ.lua
	@echo Run datalog
	time -p ../datalog -l succ.lua even.dl

clean:
	-rm succ.dl

succ.dl:	succ.awk
	awk -f succ.awk > succ.dl

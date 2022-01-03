# Aleksandr Krasnoperov

## [OT](https://en.wikipedia.org/wiki/Operational_technology) engineer

### Contact information

**Location:** Izhevsk, Russia  
**Phone:** +7 909 059-087-09  
**E-Mail:** glit6h@gmail.com  

### About

I'm a full-stack operational technology engineer who creates programs for PLC and interacting interfaces for machine operators in the dairy products industry. 

### Skills

* HTML, CSS
* Git
* IEC 61131-3 languages

### Code example

Changing time-step increment value depending on time range, 86400 equal 24h.
```
macro_command main()

unsigned int controlAxisX
unsigned int stepVol

GetData(controlAxisX, "Local HMI", LW, 0, 1)


if controlAxisX < 600 or controlAxisX >= 86400 then

	if controlAxisX <= 600 then 
		controlAxisX = 600
	//end if
	else if controlAxisX >= 86400 then 
		controlAxisX = 86400
	end if
	
else
	
	if controlAxisX >= 43200 and controlAxisX < 86400 then
		stepVol = 7200
	//end if

	else if controlAxisX >= 21600  and controlAxisX < 43200 then
		stepVol = 3600
	//end if

	else if controlAxisX >= 14400  and controlAxisX < 21600 then
		stepVol = 2400
	//end if

	else if controlAxisX >= 3600  and controlAxisX < 14400 then
		stepVol = 1800
	//end if

	else if controlAxisX >= 600  and controlAxisX < 3600 then
		stepVol = 600
		
	end if

	controlAxisX = controlAxisX + stepVol 
	
end if

SetData(controlAxisX, "Local HMI", LW, 0, 1)

end macro_command
```
### Education and courses

* Radio electronic engineer at Izhvesk State Technical University
* Siemens's courses for PLC programmers
* HTML and CSS courses at [Code-Basics.com](https://code-basics.com/)
* JS at [learn.javasript.ru](https://learn.javascript.ru/)

### English

B1 by quick check EF SET test
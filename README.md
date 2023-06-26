# Hydroponics
Python bot used for running ChemicalLoops

Config:
Figure it out on your own //TODO
MultiScreen not supported //TODO
Log, Shovel and Sprinkler can't overlap
Bot will stop at any user input


LoopLogic
 	while () {
	sprinkler_used = false
	
	scr = take_screenshot()
	found_objects = image_recognition(scr, Plants.WithoutChemical)
	if (found_objects != null) {
		collect_plants(found_objects.orderedBy(cactuse first, voraci last)
		continue
	}
	
	if (not sprinkler_used){
		sprinkler_used = true
		use_sprinkler()
		continue()
	}
	
	scr = take_screenshot()
	log_cd = character_recognition(scr)
	if (ready_to_use(log_cd)) {
		use_log_loop() // spam the same place with set interval until you don't see log board 
		sprinkler_used = false
		continue
	}
	
	found_chemicals = image_recognition(scr, Plants.WithoutChemical)
	if (found_chemicals != null) {
		max_chemical = found_chemicals.with_max(chemical.skipAmount)
		if (max_chemical.skip_amount >= log_cd){
			sprinkler_used = false
			collect_plant(max_chemical)
			continue
		}
	}
	
	break


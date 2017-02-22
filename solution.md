cd mystery
ls
cat crimescene
grep -C 4 "CLUE" crimescene
cat interviews/*
cd memberships
ls
cat AAA
cat AAdvantage
cat Delta_Skymiles
cat Museum_of_Bash_History
grep -c "" AAA
grep -c "" Delta_Skymiles
grep -f AAA Delta_Skymiles > matching_names
grep -c "" matching_names
grep -f matching_names Museum_of_Bash_History
grep -f matching_names Museum_of_Bash_History > new_matching_names
grep -f new_matching_names Terminal_City_Library > newer_matching_names
grep -c "" newer_matching_names
cd ..
grep "Annabel" people
cd streets
head -n 40 Mattapan_Street | tail -n -1
head -n 173 Hart_Place | tail -n -1
head -n 179 Buckingham_Place | tail -n -1
cd ..
cat interviews/interview-699607
grep -A 5 "L337..9" vehicles
grep -A 5 "L337..9" vehicles | grep -A 4 "Make: Honda" | grep -A 3 "Color: Blue" | grep "Owner:" > even_more_names
sed 's/Owner: //' even_more_names > most_names
grep -f most_names memberships/newer_matching_names > final_name_list
rm most_names
rm even_more_names
rm memberships/matching_names
rm memberships/new_matching_names
rm memberships/newer_matching_names
grep -f final_name_list people
#Shooter is Jeremy Bowers, since Jacqui is a woman.


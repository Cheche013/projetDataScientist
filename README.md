## Exercices Ruby part2
00_Journalists.rb : 
niv.1 -> Use handles.length to count the number of names in the list without any condition.
niv.2 -> Use handles.min (to get the shortest name) while removing the @ using h[1..-1].
niv.3 -> Here we use "count" because it counts based on a condition (in this case, names with 5 characters), although it can also work like length to count without a condition.
niv.4 ->Same principle with count, but this time we use a condition to check for uppercase letters: {|h| h[1] =~ /[A-Z]/}.
niv.5 -> If we want to keep the @, we use "sort" otherwise, we again use h[1..-1]. We also use .downcase so that sorting ignores case differences..
niv.6 -> We can use "length" here because there’s no condition 
niv.7 -> To find the position of an element, we use index, like this: handles.index("@epenser"). The idea is: if it finds the position of @epenser in the list, it returns the index; if not, it returns nil.
niv.8 -> Here, to create a distribution based on given conditions, we use a Hash that creates “bins” like : distribution[taille] ~= 1 as a counter for each size, then we loop through using each.



01_cryptocurrencies.rb : 
niv.1 -> To combine the two arrays, we need to pair the elements by position: index 0 (list 1) with index 0 (list 2).
It’s important to convert price strings into floats, so we use: s.delete(',').to_f to remove commas from numbers. I initialize my Hash and create a loop with index.
I used "p my_hash" because, unlike puts which returns nil, "p" returns the object itself. Basically, it’s for debugging, and it worked in the end.


niv.2 -> J I rewrite each list (basically copy-paste), otherwise it doesn’t work, and also for all the following exercises, add this line:  raise    "Les listes n'ont pas la même taille !" unless name.length == prices.length     
to check if the lists have different sizes, otherwise it won’t work.
Then, we find the maximum value and then all those with the same price. The idea is to determine the positions of the prices.

niv.3 -> Same principal, but now we look for values less than 6000, so we create a loop with each: cryptos_inferieur_6000.each do |name, valeur|

niv.4 -> We reuse the previous program, but now we look for the most expensive one within that subset, so we do:
cryptos_inferieur_6000 = crypto_hash.select { |_, v| v < 6000 }
crypto_plus_cher = cryptos_inferieur_6000.max_by { |_, v| v }


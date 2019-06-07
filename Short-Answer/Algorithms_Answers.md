Add your answers to the Algorithms exercises here.

a) O(n)

b) O(n^2log(n))

c) O(n)

# Exercise II

The easiest solution would be brute force dropping the egg at every floor until it goes from not break to break. This would result in O(n)

floor = 0
broke = False
highest_floor = n
for floor in range(highest_floor +1):
if drop(floor) == 'it broke':
return floor -1

return 'did not brake'

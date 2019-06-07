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
-- if drop(floor) == 'it broke':
---- return floor -1

return 'did not break'

Since the floors are naturally a sorted list we could use a binary search which would be O(log(n))

def find_floor(floor, drop):
--#check that the highest floor can not break if the highest floor cannot break it nothing lower will break it so return -1
--if drop(floor) == 'did not break':
---- return -1
--floor = floor//2
-- if drop(floor) == 'did not break' and drop(floor + 1) == 'broke':
---- return floor
-- if drop(floor) == 'broke' and drop(floor + 1) == 'broke':
---- #use the lower half
---- return find_floor(floor)
-- elif drop(floor) == 'did not break' and drop(floor + 1) == 'did not break':
---- #use upper half
---- return find_floor(floor + floor\*2)
This is not relevant to the O of a problem but I think I would do a check at the start of the search to see if the highest floor can break the egg

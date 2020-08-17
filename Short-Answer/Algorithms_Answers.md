#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a) O(n) (Linear Time)

b) O(n log n) (Quasilinear Time)

c) O(n) (Linear Time)

## Exercise II

To determine the floor I would start on the first floor (starting lower rather than higher means I will break fewer eggs).
If I throw and egg off of a floor an it survives I am going to try again 2 floors higher.
If I throw and egg from a floor and it breaks I know that I now have a range from 2 floors lower to 1 floor lower.
I will finally try the 1 floor lower to determine if that floor is good or not.
If the egg breaks that time then I know 1 floor lower than that is good since I already tested it and if it didn't break than I know the floor I am on is good.

it might look something like

def find_safe_floor():

    egg_broken == False
    f = 1

    while egg_broken == False:
        if egg_broke(f) == False:
            f += 2
        else:
            f -= 1
            egg_broken = True

    if egg_broke(f) == False:
        return f
    elif egg_broke(f):
        f -= 1
        return f

This has a runtime complexity of a constant time (assuming the floor isn't changing) or it would be N/2 since I am not checking every floor and can skip every other floor
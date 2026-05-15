package main

import "github.com/01-edu/z01"

func QuadA(x,y int)  {
	
	if x <= 0 || y <= 0 {
		return
	}

	if x == y {
		return
	}

	for Hr := 1; Hr <= y ; Hr++ {
		for Vr := 1; Vr <= x ; Vr++ {
			
			if (Hr == 1 && Vr == 1) || (Hr == 1 && Vr == x) {
				z01.PrintRune('A')	
			}else if (Hr == y && Vr == 1) || (Hr == y && Vr == x) {
				z01.PrintRune('C')
			}else if Hr == 1 || Hr == y {
				z01.PrintRune('B')
			}else if Vr == 1 || Vr == x {
				z01.PrintRune('B')
			}else {
				z01.PrintRune(' ')
			}
		}
		z01.PrintRune('\n')
	}
}
func main()  {
	QuadA(5,3)
}

# Java
Some exercise in Java
package tp3;

public class Exe3 {

	public static void aff_ligne(int n, int i) {
		//longueur max : (2*n)-1
		//condition de contour
		
		if (i == 1 || i == (2*n)-1) {           // Boundary conditions
			for (int m = 1; m < (2*n); m++ ) {
				System.out.print("1 ");
			}System.out.println();
		}else{
			if (i <=n) {
				for (int j =1; j <= i; j++) {
					System.out.print(j+" ");
				}
				if ( i == n) {
					for (int y =(i-1); y > 0; y--) {
						System.out.print(y+" ");
						
					}
				}else {
					for (int m = 1; m <= ((2*n)-1)-2*i; m++) {
						System.out.print(i+ " ");
				}
					for (int y =(i); y > 0; y--) {
						System.out.print(y+" ");
					}	
			}System.out.println();
		}
			if (i > n) {
				for (int j = 1; j <= ((2*n))-i; j++) {
					System.out.print(j+" ");
				}	
				for (int m = 1; m <-(2*n)+2*i; m++) {
					int s = 2*n-i;
					System.out.print(s+ " ");
				}
				
				for (int y = (2*n)-i; y > 0; y--) {
					System.out.print(y+" ");
				}System.out.println();
				
			}
	}
}
	public static void aff_cible(int n, int i ) {
		for(int k = 1 ; k <(2*n);k++) {
			aff_ligne(n,k);
		}
	}

	
	public static void main(String[] args) {
		// Tester ici vos fonctions
		aff_cible(2,2);
		System.out.println();
		aff_cible(3,3);
		System.out.println();
		aff_cible(4,4);
		System.out.println();
		aff_cible(5,5);
		System.out.println();
		aff_cible(9,9);
	}
}

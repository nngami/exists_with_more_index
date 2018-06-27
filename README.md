# exists_with_more_index
Modify the implementation given in order to allow an existential quantiﬁcation over more than one index variable like, for instance, exists i,j,k (a[i]>0 &amp;&amp; b[j]==1 &amp;&amp; c[k]==2).

wrong ippotesi: Ho ippotizzato che gli index_reg di ogni index deve stare tra 0 e 9. Poretrebbero stare tra [-infinito, +infinito] tipo per gestire l istruzione acse: exists i,j,k (a[10000*j-100*i + -k*i]>0 && b[j]==1 && c[k]==2). le condizione di fine sono quindi greater_than_array_size o not tra [0,9]

version_1: se  la condizione di fine sono quindi se exists è true o se è stato raggiunto il limite fisico.

versione_2: la condizione di fine è quindi se exists è true o se sono stati provati tutti i possibili valore della n-tupla di index limitato dal rispettivo arraysize dell array in cui apparve come indice, un'index per array. Es: exists i,j,k (a[i]>0 && b[j]==1 && c[k]==2)

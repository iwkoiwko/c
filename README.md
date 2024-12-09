#policja.droga.info.dzienne
#matrix_policja.drogo <- matrix(nrow = nrow(policja.droga.info.dzienne), ncol = ncol(policja.droga.info.dzienne))
#for (dane in policja.droga.info.dzienne){
#  if(is.numeric(dane) == TRUE){
 #   append(dane, matrix_policja.drogo)
  #}else if {
   # rbind(NA, matrix_policja.drogo)
  #}
#}
#print(policja.droga.info.dzienne_numerics)

policja.droga.info.dzienne_numeric <- policja.droga.info.dzienne
policja.droga.info.dzienne_numeric$dzien_tygodnia <- NULL
policja_matrix <- data.matrix(policja.droga.info.dzienne_numeric, NULL)

policja.droga.info.dzienne_char <- policja.droga.info.dzienne
policja.droga.info.dzienne_char <- policja.droga.info.dzienne$dzien_tygodnia
policja_matrix_char <- data.matrix(policja.droga.info.dzienne_char)

print(is.matrix(policja_matrix))
print(is.matrix(policja_matrix_char))

matrix_all_raport <- cbind(policja_matrix,policja_matrix_char)
df_all_raport <- data.frame(matrix_all_raport)


o <- policja.droga.info.dzienne$zatrzymani_poszukiwani
b <- policja.droga.info.dzienne$kierujacy_po_spozyciu_alkoholu
policja_kierujacy_po_spozyciu_alkoholu_zatrzymani_poszukiwani<- cbind(o,b)
licznik <- 1
print(policja_kierujacy_po_spozyciu_alkoholu_zatrzymani_poszukiwani)

for (indeks in seq_along(policja_kierujacy_po_spozyciu_alkoholu_zatrzymani_poszukiwani)) {
   if(indeks %% 50 == 0){
    
     srednia_kieruyjacy <- mean(b[1:indeks])
      mediana_kierujacy <- median(b[1:indeks])
      srednia_zatrzymani <- mean(o[1:indeks])
     miedana_zatrzymani <- median(o[1:indeks])}
      if(srednia_kieruyjacy > srednia_zatrzymani){print("średnia kierujacych jest wieksza od sredniej zatrzymanych")
     } else if {(srednia_kieruyjacy > srednia_zatrzymani){print("średnia kierujacych jest mniejsza od sredniej zatrzymanych"}
     
     
     licznik <- licznik +1
   else { next
   }  

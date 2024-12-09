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


policja.droga.info.dzienne$zatrzymani_poszukiwani
policja.droga.info.dzienne$kierujacy_po_spozyciu_alkoholu


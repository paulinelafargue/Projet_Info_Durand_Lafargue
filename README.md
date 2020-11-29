# Projet_Info_Durand_Lafargue
Projet de programmation en langage pyhton - IVP1 S1 
def main():
  if len(sys.argv) <= 2 :
    print('''Veuillez renseigner plus d'informations''')
  else :
    function = sys.argv[1]
    if function == 'Choix_Date':
      if len(sys.arg) != 4 :
        print('''Il faut renseigner une date de début et une date de fin au format 'YYYY-MM-DD'.''')
      else : 
        date_debut = str(sys.argv[2])
        date_fin = str(sys.argv[3])
        Choix_Date(date_debut, date_fin)
    if function == 'graphique':
      if len(sys.arg) != 5 :
        print('''Pour afficher le graphique d'une variable en fonction du temps, il faut renseigner :\n - une variable parmi 'lum', 'noise', 'temp', 'co2', 'humidity'\n - une date de début au format 'YYYY-MM-DD'\n - une date de fin au format 'YYYY-MM-DD'.''')
      else :
        variable = str(sys.argv[2]) 
        date_debut = str(sys.argv[3])
        date_fin = str(sys.argv[4])
        graphique(variable, date_debut, date_fin)
    if function == 'minimum':
      if len(sys.arg) != 5 :
        print('''Pour afficher le minimum d'une variable, il faut renseigner :\n - une variable parmi 'lum', 'noise', 'temp', 'co2', 'humidity'\n - une date de début au format 'YYYY-MM-DD'\n - une date de fin au format 'YYYY-MM-DD'.''')
      else :
        variable = str(sys.argv[2]) 
        date_debut = str(sys.argv[3])
        date_fin = str(sys.argv[4])
        minimum(variable, date_debut, date_fin)
    if function == 'maximum':
      if len(sys.arg) != 5 :
        print('''Pour afficher le maximum d'une variable, il faut renseigner :\n - une variable parmi 'lum', 'noise', 'temp', 'co2', 'humidity'\n - une date de début au format 'YYYY-MM-DD'\n - une date de fin au format 'YYYY-MM-DD'.''')
      else :
        variable = str(sys.argv[2]) 
        date_debut = str(sys.argv[3])
        date_fin = str(sys.argv[4])
        maximum(variable, date_debut, date_fin)
    if function == 'Fusion':
      if len(sys.arg) != 4 :
        print('''Il faut renseigner : deux listes''')
      else :
        L1 = str(sys.argv[2]) 
        L2 = str(sys.argv[3])
        Fusion(L1, L2)
    if function == 'Tri_Fusion':
      if len(sys.arg) != 5 :
        print('''Il faut renseigner : une variable (parmi 'lum', 'noise', 'temp', 'co2', 'humidity'), une date de début et une date de fin au format 'YYYY-MM-DD'.''')
      else :
        variable = str(sys.argv[2]) 
        date_debut = str(sys.argv[3])
        date_fin = str(sys.argv[4])
        Tri_Fusion(variable, date_debut, date_fin)
    if function == 'mediane':
      if len(sys.arg) != 5 :
        print('''Pour afficher le médiane d'une variable, il faut renseigner :\n - une variable parmi 'lum', 'noise', 'temp', 'co2', 'humidity'\n - une date de début au format 'YYYY-MM-DD'\n - une date de fin au format 'YYYY-MM-DD'.''')
      else :
        variable = str(sys.argv[2]) 
        date_debut = str(sys.argv[3])
        date_fin = str(sys.argv[4])
        mediane(variable, date_debut, date_fin)
    if function == 'ecart_type':
      if len(sys.arg) != 5 :
        print('''Pour afficher l'écart type des valeurs prises par une variable, il faut renseigner :\n - une variable parmi 'lum', 'noise', 'temp', 'co2', 'humidity'\n - une date de début au format 'YYYY-MM-DD'\n - une date de fin au format 'YYYY-MM-DD'.''')
      else :
        variable = str(sys.argv[2]) 
        date_debut = str(sys.argv[3])
        date_fin = str(sys.argv[4])
        ecart_type(variable, date_debut, date_fin)
    if function == 'variance':
      if len(sys.arg) != 5 :
        print('''Pour afficher la variance des valeurs prises par une variable, il faut renseigner :\n - une variable parmi 'lum', 'noise', 'temp', 'co2', 'humidity'\n - une date de début au format 'YYYY-MM-DD'\n - une date de fin au format 'YYYY-MM-DD'.''')
      else :
        variable = str(sys.argv[2]) 
        date_debut = str(sys.argv[3])
        date_fin = str(sys.argv[4])
        variance(variable, date_debut, date_fin)
    if function == 'moyenne':
      if len(sys.arg) != 5 :
        print('''Pour afficher la moyenne des valeurs prises par une variable, il faut renseigner :\n - une variable parmi 'lum', 'noise', 'temp', 'co2', 'humidity'\n - une date de début au format 'YYYY-MM-DD'\n - une date de fin au format 'YYYY-MM-DD'.''')
      else :
        variable = str(sys.argv[2]) 
        date_debut = str(sys.argv[3])
        date_fin = str(sys.argv[4])
        moyenne(variable, date_debut, date_fin)
    if function == 'moyenne':
      if len(sys.arg) != 5 :
        print('''Pour afficher la moyenne des valeurs prises par une variable, il faut renseigner :\n - une variable parmi 'lum', 'noise', 'temp', 'co2', 'humidity'\n - une date de début au format 'YYYY-MM-DD'\n - une date de fin au format 'YYYY-MM-DD'.''')
      else :
        variable = str(sys.argv[2]) 
        date_debut = str(sys.argv[3])
        date_fin = str(sys.argv[4])
        moyenne(variable, date_debut, date_fin)
    if function == 'statistiques':
      if len(sys.arg) != 5 :
        print('''Pour afficher les indicateurs statistiques des valeurs prises par une variable, il faut renseigner :\n - une variable parmi 'lum', 'noise', 'temp', 'co2', 'humidity'\n - une date de début au format 'YYYY-MM-DD'\n - une date de fin au format 'YYYY-MM-DD'.''')
      else :
        variable = str(sys.argv[2]) 
        date_debut = str(sys.argv[3])
        date_fin = str(sys.argv[4])
        statistiques(variable, date_debut, date_fin)    
    if function == 'Coef_Correlation_Spearman':
      if len(sys.arg) != 4 :
        print('''Pour afficher la valeur du coefficient de corrélation de Spearman entre les deux variables des valeurs prises par une variable, il faut renseigner :\n - 2 variable parmi 'lum', 'noise', 'temp', 'co2', 'humidity'.''')
      else :
        donnee1 = str(sys.argv[2]) 
        donnee2 = str(sys.argv[3])
        Coef_Correlation_Spearman(donnee1, donnee2)
    if function == 'Coef_Correlation_Kendall':
      if len(sys.arg) != 4 :
        print('''Pour afficher la valeur du coefficient de corrélation de Kendall entre les deux variables des valeurs prises par une variable, il faut renseigner :\n - 2 variable parmi 'lum', 'noise', 'temp', 'co2', 'humidity'.''')
      else :
        donnee1 = str(sys.argv[2]) 
        donnee2 = str(sys.argv[3])
        Coef_Correlation_Kendall(donnee1, donnee2)
    if function == 'Alpha':
      if len(sys.arg) != 4 :
        print('''Il faut renseigner une date de début et une date de fin au format 'YYYY-MM-DD'.''')
      else : 
        date_debut = str(sys.argv[2])
        date_fin = str(sys.argv[3])
        Alpha(date_debut, date_fin)
    if function == 'Point_rosee':
      if len(sys.arg) != 4 :
        print('''Il faut renseigner une date de début et une date de fin au format 'YYYY-MM-DD'.''')
      else : 
        date_debut = str(sys.argv[2])
        date_fin = str(sys.argv[3])
        Point_Rosee(date_debut, date_fin)
    if function == 'humidex':
      if len(sys.arg) != 4 :
        print('''Il faut renseigner une date de début et une date de fin au format 'YYYY-MM-DD'.''')
      else : 
        date_debut = str(sys.argv[2])
        date_fin = str(sys.argv[3])
        humidex(date_debut, date_fin)
    if function == 'anomalies':
      if len(sys.arg) != 5 :
        print('''Pour afficher graphiquement les anomalies des relevés d'une variable, il faut renseigner :\n - une variable parmi 'lum', 'noise', 'temp', 'co2', 'humidity'\n - une date de début au format 'YYYY-MM-DD'\n - une date de fin au format 'YYYY-MM-DD'.''')
      else :
        variable = str(sys.argv[2]) 
        date_debut = str(sys.argv[3])
        date_fin = str(sys.argv[4])
        anomalies(variable, date_debut, date_fin)

  
if (__name__ == 'main'):
  main()



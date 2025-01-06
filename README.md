# ALGO2
//Algorithme d'insertion

function insertionSort(arr) {
    // Parcourir chaque élément du tableau à partir du deuxième
    for (let i = 1; i < arr.length; i++) {
        let key = arr[i]; // Élément à insérer
        let j = i - 1;

        // Déplacer les éléments de la séquence triée qui sont plus grands que key
        while (j >= 0 && arr[j] > key) {
            arr[j + 1] = arr[j]; // Décaler l'élément vers la droite
            j--;
        }

        // Insérer l'élément à sa position correcte
        arr[j + 1] = key;
    }

    return arr; // Retourner le tableau trié
}

// Exemple d'utilisation
const tableau = [12, 11, 13, 5, 6];
console.log("Tableau non trié :", tableau);
const tableauTrie = insertionSort(tableau);
console.log("Tableau trié :", tableauTrie);

END

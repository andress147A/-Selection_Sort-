Selection_Sort
O Selection Sort ordena a lista encontrando o menor elemento e trocando-o com a primeira posição, depois repete o processo para o restante da lista. Sua complexidade é O(n²) no pior caso, tornando-o ineficiente para grandes conjuntos de dados, mas útil quando trocas de elementos precisam ser minimizadas.



public class SelectionSort {
    public static void selectionSort(int[] arr) {
        int n = arr.length;
          for (int i = 0; i < n - 1; i++) {
            int minIndex = i;
            for (int j = i + 1; j < n; j++) {
                if (arr[j] < arr[minIndex]) {
                    minIndex = j;
                }
            }
            int temp = arr[minIndex];
            arr[minIndex] = arr[i];
            arr[i] = temp;
            System.out.print("Etapa " + (i + 1) + ": ");
            printArray(arr);
        }
       
    }
    public static void main(String[] args) {
        int[] arr = {64, 25, 12, 22, 11};
        System.out.println("Array antes da ordenação:");
        printArray(arr);
        selectionSort(arr);
        System.out.println("Array após a ordenação:");
        printArray(arr);
    }
    private static void printArray(int[] arr) {
        for (int num : arr) {
            System.out.print(num + " ");
        }
        System.out.println();
    }
}


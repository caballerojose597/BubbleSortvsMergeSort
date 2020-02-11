# BubbleSortvsMergeSort
proyecto EDD
public class Main {

    public static int[] main(String[] args){
        // Codigo del Bubble Sort
        public int [] bubbleSort(int[]arr){
            for (int i = 0; i <arr.length ; i++) {
                for (int j = 0; j <arr.length ; j++) {
                    if(arr[j]<arr[i]){
                        int temp = arr[j];
                        arr[i] = arr[j];
                        arr[j] = temp;
                    }
                }
            }
            return arr;
        }

        // Codigo Merge Sort
        public int[] merge(int []a, int[]b){
            int [] c = new int[a.length + b.length];
            int j =0, k = 0, i;
            for (i = 0; i < c.length && j < a.length && k < b.length; i++) {
                if(a[j] < b[k]){
                    c[i] = a[j++];
                }
                else{
                    c[i] = b[k++];
                }

            }

            for(; i< c.length;i++){
                if(j<a.length){
                    c[i] = a[j++];
                }
                if(k<b.length){
                    if(k<b.length){
                        c[i] = b[k++];
                    }
                }
            }


            return c;
        }

        public int [] mergeSort(int[] array){
            // caso base
            if(array.length == 1)
                return array;

            int[] parteInferior = new int[array.length/2];
            int[] parteSuperior = new int[array.length - parteInferior.length];
            int i = 0;

            for (; i < parteInferior.length; i++) {
                parteInferior[i] = array[i];
            }

            for (int j = 0; j < parteSuperior.length; j++) {
                parteSuperior[j] = array[i+j];
            }
    }
}

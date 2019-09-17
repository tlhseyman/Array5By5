package sample;

public class Array5x5 {
    public static void main(String[] args) {
        int[][] myImage = {
                          {0,18,238,255,248},
                          {0,87,255,255,255},
                          {0,75,255,255,255},
                         {0,39,255,255,255},
                          {0,67,255,255,255}
                 };
        findAllEdges(myImage);

    }
    public static void findAllEdges(int[][] image){
        int[][] diffs = new int[image.length][image[0].length];
        for(int i=0; i<image.length; i++){
            for(int j=1; j<image[i].length; j++){
                diffs[i][j] = Math.abs(image[i][j] - image[i][j-1]);
            }
        }
        for(int i=0; i<diffs.length; i++){
            for(int j=0; j<diffs[i].length; j++){
                System.out.print(diffs[i][j]+",");
            }
            System.out.println();
        }
    }
}

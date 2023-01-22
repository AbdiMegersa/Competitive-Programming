class Solution {
    public int leastInterval(char[] tasks, int n) {
     int[] rep=new int[26];
        for(char c:tasks){
            rep[c-'A']++;
        }
        Arrays.sort(rep);
        int last=rep[25]-1;
        int idle=last*n;
        for(int i=24; i>=0; i--){
            idle-=Math.min(rep[i],last);
        }
        return idle>0 ? idle+tasks.length : tasks.length;
    }
}

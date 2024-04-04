package winsoft;

import java.util.HashMap;
import java.util.Map;

public class DuplicateCharacters {
	 public static void main(String[] args) {
	        String str = "hello world";
	        findDuplicateCharacters(str);
	    }

	    public static void findDuplicateCharacters(String str) {
	        
	        Map<Character, Integer> charCountMap = new HashMap<>();

	      
	        char[] charArray = str.toCharArray();

	       
	        for (char c : charArray) {
	            if (charCountMap.containsKey(c)) {
	                charCountMap.put(c, charCountMap.get(c) + 1);
	            } else {
	            
	            charCountMap.put(c, 1);
	            }
	        }

	        // Displaying duplicate characters
	        System.out.println("Duplicate characters in the string '" + str + "':");
	        for (Map.Entry<Character, Integer> entry : charCountMap.entrySet()) {
	            if (entry.getValue() > 1) {
	                System.out.println(entry.getKey() + " : " + entry.getValue() + " times");
	            }
	        }
	    }
}

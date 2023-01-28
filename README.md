#Solutions For python And React question Set

Python Question 1 solution
def lcsubstr(str1, str2):
    	ans = 0;

	for i in range(len(str1)):
         for j in range(len(str2)):
		k = 0;
		while ((i + k) < len(str1) and (j + k) < len(str2) 
				and str1[i + k] == str2[j + k]): 
			k = k + 1;

		ans = max(ans, k);
      return ans;
      

Python 2nd Question solution

def pairsum(list, target):
    result = []
    loop = 1
    for x in list:
        for y in list:
            if x + y == target:
                result.append((x, y))
        list = list[loop:]
        loop += 1
    return result
    


Javascript 1st Question solution
    
function longest_common_starting_substring(arr1){
var arr= arr1.concat().sort(),
a1= arr[0], a2= arr[arr.length-1], L= a1.length, i= 0;
while(i< L && a1.charAt(i)=== a2.charAt(i)) i++;
return a1.substring(0, i);
}


Javascript 2nd Question solution

function findTwoSum(numbers, sum) {
  let indices = [];
  for (let i = 0; i < numbers.length; i++) {
    for (let j = i + 1; j < numbers.length; j++) {
      if (numbers[i] + numbers[j] === sum)
        indices.push([numbers[i], numbers[j]]);
    }
  }
  return indices;
}

const indices = findTwoSum([3, 1, 5, 7, 5, 9], 10);
console.log(indices);

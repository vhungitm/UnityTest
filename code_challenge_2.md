var findLength = function(nums1, nums2) {
  let maxLength = 0
  for (let i = 0; i < nums1.length; i++) {
    for (let j = 0; j < nums2.length; j++) {
      if (nums1[i] == nums2[j]) {
        let arrayLength = 1
        for (let z = 1; (i + z < nums1.length) && (j + z < nums2.length); z++) {
          if (nums1[i + z] != nums2[j + z])
            break
          arrayLength += 1
        }
        if (arrayLength > maxLength)
          maxLength = arrayLength
      }
    }
  }
  return maxLength
}

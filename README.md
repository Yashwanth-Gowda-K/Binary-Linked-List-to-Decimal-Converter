# Binary-Linked-List-to-Decimal-Converter


onvert a binary number represented as a linked list to its decimal equivalent efficiently using bitwise operations.

## Problem Statement
Given the head of a singly linked list where each node contains a single binary digit (0 or 1), return the corresponding decimal value.

### Examples
- Input: `1 → 0 → 1`  
  Output: `5` (1×2² + 0×2¹ + 1×2⁰ = 5)
- Input: `1 → 0 → 0 → 1`  
  Output: `9` (1×2³ + 0×2² + 0×2¹ + 1×2⁰ = 9)

## 🚀 Solution Approach

### Optimal Method: Bit Shifting
- **Time Complexity**: O(n) - Single pass through the linked list
- **Space Complexity**: O(1) - No additional space required

**Key Steps**:
1. Initialize `result = 0`
2. Traverse the linked list:
   - Left-shift `result` (equivalent to multiplying by 2)
   - Bitwise OR with current node's value (adds the bit)
3. Return final decimal value

### Alternative Method
Also includes arithmetic implementation for better readability:
```python
result = result * 2 + head.val

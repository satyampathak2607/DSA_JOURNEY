# Topics_Covered:-

1. Check if a string is Palindrome or not using recursion

## SNIPPET
    s = "nitin"
    def palindrome_check(s,L,R):
        if L >= R:
            return True
        if s[L] != s[R]:
            return False
        return palindrome_check(s,L+1,R-1)

    palindrome_check(s,0,len(s)-1)


## EXPLANATION

### Base Case
    If the two pointers have met (L == R, odd length)
    or crossed (L > R, even length)
    
### MISMATCH CHECK

    if s[L] != s[R]:
        return False
  .

    If any pair doesn’t match,
    no point checking the rest — it’s already broken.

### RECURSION

    "nitin"  → compare 'n' == 'n' ✅  → now check "iti"
    "iti"    → compare 'i' == 'i' ✅  → now check "t"
    "t"      → L==R ✅  base case → True

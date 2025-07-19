# Competitive_Programming

## Important Points

- There is is_sorted function in codeforces with O(n) complexity for arrays and vectors


## Ideas
- Binary search on Answer
- there is a problem in which we jump from one segment(li,ri) to the other segement(l(i+1),r(i+1)) with jump distance of atmost k.we can check the feasibility of    k (possible or not for k) by maintaining two variables which tracks the minimum distance and max distance the can be achieved  on the next segment.
<pre>
def check(k):
    ll, rr = 0, 0  # Initialize left and right bounds

    for e in seg:
        # Expand or adjust the bounds with margin k
        ll = max(ll - k, e[0])
        rr = min(rr + k, e[1])

        # If the interval becomes invalid
        if ll > rr:
            return False

    return True
</pre>

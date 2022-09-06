<div align="center">
    <h1>Arrays</h1>
</div>

<ol>
    <li>

        **let array = [1, 2, 3, 4, 5, 6];**
        **let [a, b, , ...rest] = array;**

        ****
        **console.log(a)**
        **console.log(b)**
        **console.log(c)**
        **console.log(rest)**
        ****
        **let c;**

        - A: `1, 2, 3, [ 4, 5, 6 ]`
        - B: `1, 2, c is not defined`
        - C: `1, 2, NaN, undefined`
        - D: `1, 2, c is not defined, [4, 5, 6]`

        <br />
        <details>
            <summary><b>Answer</b></summary>
            <p>

                #### Option: B

            </p>
        </details>
    </li>

    ---

    <li>

        **let array1 = [1, 2, 3, 4, 5, 6];**
        **let array2 = array1**

        ****
        **array2.push(7, 8, 9, 10)**
        **console.log(array1)**
        **console.log(array2.sort())**

        - A: `[ 1, 2, 3, 4, 5, 6 ], [ 1, 10, 2, 3, 4, 5, 6, 7, 7, 8, 8, 9, 9 ]`
        - B: `[ 1, 2, 3, 4, 5, 6, 7, 8, 9, 7, 8, 9, 10 ], [ 1, 10, 2, 3, 4, 5, 6, 7, 7, 8, 8, 9, 9 ]`
        - C: `[ 1, 2, 3, 4, 5, 6, 7, 8, 9, 7, 8, 9, 10 ], [ 1, 2, 3, 4, 5, 6, 7, 7, 8, 8, 9, 9, 10 ]`
        - D: `[ 1, 2, 3, 4, 5, 6, 7, 8, 9, 7, 8, 9, 10 ], [ 1, 2, 3, 4, 5, 6 ]`

        <br />
        <details>
            <summary><b>Answer</b></summary>
            <p>

                #### Option: B

            </p>
        </details>
    </li>

</ol>
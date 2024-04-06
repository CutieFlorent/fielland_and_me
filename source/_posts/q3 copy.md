提问：

- 0.Florent 很可爱
- 1.{你对问题 0 撒谎了}、{你对问题 2 撒谎了}和{我想要的问题 1}奇数个为真。
- 2.{你对问题 0 撒谎了}、{你对问题 1 撒谎了}和{我想要的问题 2}奇数个为真。

将问题本身的真值记作$q_n$，问题是否撒谎记作$l_n$，对问题的回答记作$a_n$，易得$a_n = l_n \oplus q_n$.同时，自己想要的问题记作$w_n$，所以目标是用$a_n$表示出$w_n$.
可以得到：
$
\begin{cases}
    q_0 = \text{true} \\
    q_1 = l_0 \oplus l_2 \oplus w_1\\
    q_2 = l_0 \oplus l_1 \oplus w_2\\
\end{cases} \Rightarrow
\begin{cases}
    a_0 = \neg l_0\\
    a_1 = l_1 \oplus l_0 \oplus l_2 \oplus w_1\\
    a_2 = l_2 \oplus l_0 \oplus l_1 \oplus w_2\\
\end{cases}
$
由于三个问题只有一个撒谎，故$l_0 \oplus l_1 \oplus l_2$为真，所以：
$
\begin{cases}
    a_0 = \neg l_0\\
    a_1 = \neg w_1\\
    a_2 = \neg w_2\\
\end{cases}\Rightarrow
\begin{cases}
    w_1 = \neg a_1\\
    w_2 = \neg a_2\\
\end{cases}
$
$
看问 1 和问 2 的答案取反即可.

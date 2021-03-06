<h3 id="数组">数组</h3>
<ul>
<li>旋转数组的最小数字</li>
</ul>
<pre class=" language-py"><code class="prism  language-py"><span class="token comment" spellcheck="true"># -*- coding:utf-8 -*-</span>
<span class="token comment" spellcheck="true"># 所有元素都是大于0， 所以零pre=0</span>
<span class="token keyword">class</span> <span class="token class-name">Solution</span><span class="token punctuation">:</span>
    <span class="token keyword">def</span> <span class="token function">minNumberInRotateArray</span><span class="token punctuation">(</span>self<span class="token punctuation">,</span> rotateArray<span class="token punctuation">)</span><span class="token punctuation">:</span>
        <span class="token keyword">if</span> len<span class="token punctuation">(</span>rotateArray<span class="token punctuation">)</span><span class="token operator">==</span><span class="token number">0</span><span class="token punctuation">:</span>
            <span class="token keyword">return</span> <span class="token number">0</span>
        pre <span class="token operator">=</span> <span class="token number">0</span>
        <span class="token keyword">for</span> num <span class="token keyword">in</span> rotateArray<span class="token punctuation">:</span>
            <span class="token keyword">if</span> num <span class="token operator">&lt;</span> pre<span class="token punctuation">:</span>
                <span class="token keyword">return</span> num
            pre <span class="token operator">=</span> num
        <span class="token keyword">return</span> rotateArray<span class="token punctuation">[</span><span class="token number">0</span><span class="token punctuation">]</span> 
        <span class="token comment" spellcheck="true">#  有序，输出第一个元素</span>
</code></pre>
<h3 id="字符串">字符串</h3>
<ul>
<li>替换空格</li>
</ul>
<pre class=" language-py"><code class="prism  language-py"><span class="token comment" spellcheck="true"># -*- coding:utf-8 -*-</span>
<span class="token keyword">class</span> <span class="token class-name">Solution</span><span class="token punctuation">:</span>
    <span class="token comment" spellcheck="true"># s 源字符串</span>
    <span class="token keyword">def</span> <span class="token function">replaceSpace</span><span class="token punctuation">(</span>self<span class="token punctuation">,</span> s<span class="token punctuation">)</span><span class="token punctuation">:</span>
        <span class="token keyword">return</span> s<span class="token punctuation">.</span>replace<span class="token punctuation">(</span><span class="token string">' '</span><span class="token punctuation">,</span> <span class="token string">'%20'</span><span class="token punctuation">)</span>
</code></pre>
<h3 id="链表">链表</h3>
<ul>
<li>反转链表</li>
</ul>
<pre class=" language-py"><code class="prism  language-py"><span class="token comment" spellcheck="true"># -*- coding:utf-8 -*-</span>
<span class="token comment" spellcheck="true"># class ListNode:</span>
<span class="token comment" spellcheck="true">#     def __init__(self, x):</span>
<span class="token comment" spellcheck="true">#         self.val = x</span>
<span class="token comment" spellcheck="true">#         self.next = None</span>
<span class="token keyword">class</span> <span class="token class-name">Solution</span><span class="token punctuation">:</span>
    <span class="token comment" spellcheck="true"># 返回ListNode</span>
    <span class="token keyword">def</span> <span class="token function">ReverseList</span><span class="token punctuation">(</span>self<span class="token punctuation">,</span> pHead<span class="token punctuation">)</span><span class="token punctuation">:</span>
        <span class="token keyword">if</span> <span class="token operator">not</span> pHead <span class="token operator">or</span> <span class="token operator">not</span> pHead<span class="token punctuation">.</span>next<span class="token punctuation">:</span> <span class="token comment" spellcheck="true"># 空或者只有一个元素直接返回</span>
            <span class="token keyword">return</span> pHead
        q <span class="token operator">=</span> None
        p <span class="token operator">=</span> pHead
        <span class="token keyword">while</span> p<span class="token punctuation">:</span>
            tmp <span class="token operator">=</span> p<span class="token punctuation">.</span>next <span class="token comment" spellcheck="true">#暂存下一个结点</span>
            p<span class="token punctuation">.</span>next <span class="token operator">=</span> q <span class="token comment" spellcheck="true"># 修改当前结点指向</span>
            q <span class="token operator">=</span> p <span class="token comment" spellcheck="true"># 指向返回链表的第一个元素</span>
            p <span class="token operator">=</span> tmp <span class="token comment" spellcheck="true"># 访问下一个</span>
        <span class="token keyword">return</span> q
        <span class="token comment" spellcheck="true"># write code here</span>
</code></pre>
<ul>
<li>链表中倒数第k个结点</li>
</ul>
<pre class=" language-py"><code class="prism  language-py"><span class="token comment" spellcheck="true"># -*- coding:utf-8 -*-</span>
<span class="token comment" spellcheck="true"># class ListNode:</span>
<span class="token comment" spellcheck="true">#     def __init__(self, x):</span>
<span class="token comment" spellcheck="true">#         self.val = x</span>
<span class="token comment" spellcheck="true">#         self.next = None</span>

<span class="token keyword">class</span> <span class="token class-name">Solution</span><span class="token punctuation">:</span>
    <span class="token keyword">def</span> <span class="token function">FindKthToTail</span><span class="token punctuation">(</span>self<span class="token punctuation">,</span> head<span class="token punctuation">,</span> k<span class="token punctuation">)</span><span class="token punctuation">:</span>
    <span class="token comment" spellcheck="true"># 链表k可能大于链表长度，此时返回None</span>
        i <span class="token operator">=</span> <span class="token number">0</span>
        p <span class="token operator">=</span> head
        <span class="token keyword">while</span> p <span class="token operator">and</span> i<span class="token operator">&lt;</span>k<span class="token punctuation">:</span>
            p <span class="token operator">=</span> p<span class="token punctuation">.</span>next
            i <span class="token operator">+=</span> <span class="token number">1</span>
      
        <span class="token keyword">if</span> i<span class="token operator">==</span>k<span class="token punctuation">:</span>  <span class="token comment" spellcheck="true"># k小于等于链表长度，正常处理</span>
            q <span class="token operator">=</span> head
            <span class="token keyword">while</span> p<span class="token punctuation">:</span>
                q <span class="token operator">=</span> q<span class="token punctuation">.</span>next
                p <span class="token operator">=</span> p<span class="token punctuation">.</span>next
            <span class="token keyword">return</span> q
        <span class="token keyword">return</span> None
        <span class="token comment" spellcheck="true"># write code here</span>
</code></pre>
<ul>
<li>从尾到头打印链表</li>
</ul>
<pre class=" language-py"><code class="prism  language-py"><span class="token comment" spellcheck="true"># -*- coding:utf-8 -*-</span>
<span class="token comment" spellcheck="true"># class ListNode:</span>
<span class="token comment" spellcheck="true">#     def __init__(self, x):</span>
<span class="token comment" spellcheck="true">#         self.val = x</span>
<span class="token comment" spellcheck="true">#         self.next = None</span>
<span class="token keyword">from</span> collections <span class="token keyword">import</span> deque
<span class="token keyword">class</span> <span class="token class-name">Solution</span><span class="token punctuation">:</span>
    <span class="token comment" spellcheck="true"># 返回从尾部到头部的列表值序列，例如[1,2,3]</span>
    <span class="token keyword">def</span> <span class="token function">printListFromTailToHead</span><span class="token punctuation">(</span>self<span class="token punctuation">,</span> listNode<span class="token punctuation">)</span><span class="token punctuation">:</span>
        <span class="token keyword">if</span> <span class="token operator">not</span> listNode<span class="token punctuation">:</span>
            <span class="token keyword">return</span> <span class="token punctuation">[</span><span class="token punctuation">]</span>
        tmp <span class="token operator">=</span> deque<span class="token punctuation">(</span><span class="token punctuation">)</span>  <span class="token comment" spellcheck="true">#　使用队列</span>
        <span class="token keyword">while</span> listNode<span class="token punctuation">:</span>
            tmp<span class="token punctuation">.</span>appendleft<span class="token punctuation">(</span>listNode<span class="token punctuation">.</span>val<span class="token punctuation">)</span>
            listNode <span class="token operator">=</span> listNode<span class="token punctuation">.</span>next
        <span class="token keyword">return</span> tmp
        <span class="token comment" spellcheck="true"># write code here</span>
</code></pre>
<h3 id="栈和队列">栈和队列</h3>
<h3 id="递归和循环">递归和循环</h3>
<ul>
<li>矩阵覆盖</li>
<li>变态跳台阶</li>
<li>跳台阶</li>
</ul>
<pre class=" language-py"><code class="prism  language-py"><span class="token comment" spellcheck="true"># -*- coding:utf-8 -*-</span>
<span class="token keyword">class</span> <span class="token class-name">Solution</span><span class="token punctuation">:</span>
    <span class="token keyword">def</span> <span class="token function">jumpFloor</span><span class="token punctuation">(</span>self<span class="token punctuation">,</span> number<span class="token punctuation">)</span><span class="token punctuation">:</span>
        a <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token number">0</span><span class="token punctuation">,</span><span class="token number">1</span><span class="token punctuation">,</span><span class="token number">2</span><span class="token punctuation">]</span> <span class="token comment" spellcheck="true"># 起步不一样</span>
        <span class="token keyword">if</span> number<span class="token operator">&lt;</span><span class="token number">3</span><span class="token punctuation">:</span>
            <span class="token keyword">return</span> a<span class="token punctuation">[</span>number<span class="token punctuation">]</span>
        <span class="token keyword">for</span> i <span class="token keyword">in</span> xrange<span class="token punctuation">(</span><span class="token number">3</span><span class="token punctuation">,</span> number<span class="token operator">+</span><span class="token number">1</span><span class="token punctuation">)</span><span class="token punctuation">:</span>
            a<span class="token punctuation">.</span>append<span class="token punctuation">(</span>a<span class="token punctuation">[</span>i<span class="token number">-1</span><span class="token punctuation">]</span><span class="token operator">+</span>a<span class="token punctuation">[</span>i<span class="token number">-2</span><span class="token punctuation">]</span><span class="token punctuation">)</span>
        <span class="token keyword">return</span> a<span class="token punctuation">[</span>number<span class="token punctuation">]</span>
        <span class="token comment" spellcheck="true"># write code here</span>
</code></pre>
<ul>
<li>斐波拉契数列</li>
</ul>
<pre class=" language-py"><code class="prism  language-py"><span class="token comment" spellcheck="true"># -*- coding:utf-8 -*-</span>
<span class="token comment" spellcheck="true"># 使用记忆体函数，保存中间值。</span>
<span class="token keyword">from</span> functools <span class="token keyword">import</span> wraps

<span class="token keyword">def</span> <span class="token function">memo</span><span class="token punctuation">(</span>func<span class="token punctuation">)</span><span class="token punctuation">:</span>
    cache <span class="token operator">=</span> <span class="token punctuation">{</span><span class="token punctuation">}</span>
    @wraps<span class="token punctuation">(</span>func<span class="token punctuation">)</span>
    <span class="token keyword">def</span> <span class="token function">wrap</span><span class="token punctuation">(</span><span class="token operator">*</span>args<span class="token punctuation">)</span><span class="token punctuation">:</span>
        <span class="token keyword">if</span> args <span class="token operator">not</span> <span class="token keyword">in</span> cache<span class="token punctuation">:</span>
            cache<span class="token punctuation">[</span>args<span class="token punctuation">]</span> <span class="token operator">=</span> func<span class="token punctuation">(</span><span class="token operator">*</span>args<span class="token punctuation">)</span>
        <span class="token keyword">return</span> cache<span class="token punctuation">[</span>args<span class="token punctuation">]</span>
    <span class="token keyword">return</span> wrap

<span class="token keyword">class</span> <span class="token class-name">Solution</span><span class="token punctuation">:</span>
    @memo
    <span class="token keyword">def</span> <span class="token function">Fibonacci</span><span class="token punctuation">(</span>self<span class="token punctuation">,</span> n<span class="token punctuation">)</span><span class="token punctuation">:</span>
        <span class="token keyword">if</span> n<span class="token operator">==</span><span class="token number">0</span><span class="token punctuation">:</span>
            <span class="token keyword">return</span> <span class="token number">0</span>
        <span class="token keyword">if</span> n<span class="token operator">&lt;</span><span class="token number">2</span><span class="token punctuation">:</span>
            <span class="token keyword">return</span> <span class="token number">1</span>
        <span class="token keyword">return</span> self<span class="token punctuation">.</span>Fibonacci<span class="token punctuation">(</span>n<span class="token number">-1</span><span class="token punctuation">)</span> <span class="token operator">+</span> self<span class="token punctuation">.</span>Fibonacci<span class="token punctuation">(</span>n<span class="token number">-2</span><span class="token punctuation">)</span>
       
<span class="token comment" spellcheck="true"># 使用list缓存中间值</span>
<span class="token keyword">class</span> <span class="token class-name">Solution_2</span><span class="token punctuation">:</span>
    <span class="token keyword">def</span> <span class="token function">Fibonacci</span><span class="token punctuation">(</span>self<span class="token punctuation">,</span> n<span class="token punctuation">)</span><span class="token punctuation">:</span>
        a <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token number">0</span><span class="token punctuation">,</span> <span class="token number">1</span><span class="token punctuation">,</span> <span class="token number">1</span><span class="token punctuation">]</span>
        <span class="token keyword">if</span> n<span class="token operator">&lt;</span><span class="token number">3</span><span class="token punctuation">:</span>
            <span class="token keyword">return</span> a<span class="token punctuation">[</span>n<span class="token punctuation">]</span>
        <span class="token keyword">for</span> i <span class="token keyword">in</span> range<span class="token punctuation">(</span><span class="token number">3</span><span class="token punctuation">,</span>n<span class="token operator">+</span><span class="token number">1</span><span class="token punctuation">)</span><span class="token punctuation">:</span>
            a<span class="token punctuation">.</span>append<span class="token punctuation">(</span>a<span class="token punctuation">[</span>i<span class="token number">-1</span><span class="token punctuation">]</span><span class="token operator">+</span>a<span class="token punctuation">[</span>i<span class="token number">-2</span><span class="token punctuation">]</span><span class="token punctuation">)</span>
        <span class="token keyword">return</span> a<span class="token punctuation">[</span>n<span class="token punctuation">]</span>
        
</code></pre>
<h3 id="树">树</h3>
<ul>
<li>重建二叉树：给出前序和中序</li>
</ul>
<pre class=" language-py"><code class="prism  language-py"><span class="token comment" spellcheck="true"># -*- coding:utf-8 -*-</span>
<span class="token comment" spellcheck="true"># class TreeNode:</span>
<span class="token comment" spellcheck="true">#     def __init__(self, x):</span>
<span class="token comment" spellcheck="true">#         self.val = x</span>
<span class="token comment" spellcheck="true">#         self.left = None</span>
<span class="token comment" spellcheck="true">#         self.right = None</span>
<span class="token keyword">class</span> <span class="token class-name">Solution</span><span class="token punctuation">:</span>
    <span class="token comment" spellcheck="true"># 返回构造的TreeNode根节点</span>
    <span class="token keyword">def</span> <span class="token function">reConstructBinaryTree</span><span class="token punctuation">(</span>self<span class="token punctuation">,</span> pre<span class="token punctuation">,</span> tin<span class="token punctuation">)</span><span class="token punctuation">:</span>
        <span class="token keyword">if</span> <span class="token operator">not</span> pre <span class="token operator">or</span> <span class="token operator">not</span> tin<span class="token punctuation">:</span>
            <span class="token keyword">return</span> None
        root <span class="token operator">=</span> TreeNode<span class="token punctuation">(</span>pre<span class="token punctuation">[</span><span class="token number">0</span><span class="token punctuation">]</span><span class="token punctuation">)</span>
        idx <span class="token operator">=</span> tin<span class="token punctuation">.</span>index<span class="token punctuation">(</span>pre<span class="token punctuation">[</span><span class="token number">0</span><span class="token punctuation">]</span><span class="token punctuation">)</span>
        left <span class="token operator">=</span> self<span class="token punctuation">.</span>reConstructBinaryTree<span class="token punctuation">(</span>pre<span class="token punctuation">[</span><span class="token number">1</span><span class="token punctuation">:</span>idx<span class="token operator">+</span><span class="token number">1</span><span class="token punctuation">]</span><span class="token punctuation">,</span> tin<span class="token punctuation">[</span><span class="token punctuation">:</span>idx<span class="token punctuation">]</span><span class="token punctuation">)</span> <span class="token comment" spellcheck="true"># 递归处理左子树</span>
        right <span class="token operator">=</span> self<span class="token punctuation">.</span>reConstructBinaryTree<span class="token punctuation">(</span>pre<span class="token punctuation">[</span>idx<span class="token operator">+</span><span class="token number">1</span><span class="token punctuation">:</span><span class="token punctuation">]</span><span class="token punctuation">,</span> tin<span class="token punctuation">[</span>idx<span class="token operator">+</span><span class="token number">1</span><span class="token punctuation">:</span><span class="token punctuation">]</span><span class="token punctuation">)</span>　<span class="token comment" spellcheck="true"># 递归处理右子树</span>
        <span class="token keyword">if</span> left<span class="token punctuation">:</span>
            root<span class="token punctuation">.</span>left <span class="token operator">=</span> left
        <span class="token keyword">if</span> right<span class="token punctuation">:</span>
            root<span class="token punctuation">.</span>right <span class="token operator">=</span> right
        <span class="token keyword">return</span> root
        <span class="token comment" spellcheck="true"># write code here</span>
</code></pre>
<h3 id="数值运算">数值运算</h3>
<ul>
<li>调整数组顺序使奇数位于偶数前面</li>
</ul>
<pre class=" language-py"><code class="prism  language-py"><span class="token comment" spellcheck="true"># -*- coding:utf-8 -*-</span>
<span class="token keyword">class</span> <span class="token class-name">Solution</span><span class="token punctuation">:</span>
    <span class="token keyword">def</span> <span class="token function">reOrderArray</span><span class="token punctuation">(</span>self<span class="token punctuation">,</span> array<span class="token punctuation">)</span><span class="token punctuation">:</span>
        <span class="token comment" spellcheck="true"># write code here</span>
        num1 <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token punctuation">]</span>
        num2 <span class="token operator">=</span> <span class="token punctuation">[</span><span class="token punctuation">]</span>
        <span class="token keyword">for</span> num <span class="token keyword">in</span> array<span class="token punctuation">:</span>
            <span class="token keyword">if</span> num<span class="token operator">&amp;</span><span class="token number">0x1</span><span class="token operator">==</span><span class="token number">0</span><span class="token punctuation">:</span> <span class="token comment" spellcheck="true"># 利用位运算判断奇偶</span>
                num1<span class="token punctuation">.</span>append<span class="token punctuation">(</span>num<span class="token punctuation">)</span>
            <span class="token keyword">else</span><span class="token punctuation">:</span>
                num2<span class="token punctuation">.</span>append<span class="token punctuation">(</span>num<span class="token punctuation">)</span>
        <span class="token keyword">return</span> num2<span class="token operator">+</span>num1
</code></pre>
<ul>
<li>数值的整数次方</li>
</ul>
<blockquote>
<p>指数可能正也可能负</p>
</blockquote>
<pre class=" language-py"><code class="prism  language-py"><span class="token comment" spellcheck="true"># -*- coding:utf-8 -*-</span>
 
<span class="token keyword">class</span> <span class="token class-name">Solution</span><span class="token punctuation">:</span>
    <span class="token keyword">def</span> <span class="token function">Power</span><span class="token punctuation">(</span>self<span class="token punctuation">,</span> base<span class="token punctuation">,</span> exponent<span class="token punctuation">)</span><span class="token punctuation">:</span>
        <span class="token keyword">if</span> exponent <span class="token operator">==</span> <span class="token number">0</span><span class="token punctuation">:</span>
            <span class="token keyword">return</span> <span class="token number">1</span>
        <span class="token keyword">if</span> exponent <span class="token operator">==</span> <span class="token number">1</span><span class="token punctuation">:</span>
            <span class="token keyword">return</span> base
        exp <span class="token operator">=</span> abs<span class="token punctuation">(</span>exponent<span class="token punctuation">)</span>
        result <span class="token operator">=</span> self<span class="token punctuation">.</span>Power<span class="token punctuation">(</span>base<span class="token punctuation">,</span> exp<span class="token operator">&gt;&gt;</span><span class="token number">1</span><span class="token punctuation">)</span>  <span class="token comment" spellcheck="true"># 处理exp/2的情况</span>
        result <span class="token operator">*=</span> result
        <span class="token keyword">if</span> <span class="token punctuation">(</span>exp <span class="token operator">&amp;</span> <span class="token number">0x1</span> <span class="token operator">==</span> <span class="token number">1</span><span class="token punctuation">)</span><span class="token punctuation">:</span> <span class="token comment" spellcheck="true"># 最后一位是1还需要* base 奇数个base的情况</span>
            result <span class="token operator">*=</span> base
        <span class="token keyword">if</span> exponent <span class="token operator">&gt;</span> <span class="token number">0</span><span class="token punctuation">:</span>
            <span class="token keyword">return</span> result
        <span class="token keyword">return</span> <span class="token number">1</span><span class="token operator">/</span>result
</code></pre>
<ul>
<li>二进制中1的个数</li>
</ul>
<pre class=" language-py"><code class="prism  language-py"><span class="token comment" spellcheck="true"># -*- coding:utf-8 -*-</span>
<span class="token keyword">class</span> <span class="token class-name">Solution</span><span class="token punctuation">:</span>
    <span class="token keyword">def</span> <span class="token function">NumberOf1</span><span class="token punctuation">(</span>self<span class="token punctuation">,</span> n<span class="token punctuation">)</span><span class="token punctuation">:</span>
        <span class="token comment" spellcheck="true"># 内建bin转换为二进制统计1的个数,注意处理正负号的情况</span>
        <span class="token keyword">if</span> n<span class="token operator">==</span><span class="token number">0</span><span class="token punctuation">:</span>
            <span class="token keyword">return</span> <span class="token number">0</span>
        <span class="token keyword">if</span> n<span class="token operator">&gt;</span><span class="token number">0</span><span class="token punctuation">:</span>
            <span class="token keyword">return</span> bin<span class="token punctuation">(</span>n<span class="token punctuation">)</span><span class="token punctuation">.</span>count<span class="token punctuation">(</span><span class="token string">'1'</span><span class="token punctuation">)</span>
        <span class="token keyword">else</span><span class="token punctuation">:</span>
            <span class="token keyword">return</span> bin<span class="token punctuation">(</span>n<span class="token operator">&amp;</span><span class="token number">0xffffffff</span><span class="token punctuation">)</span><span class="token punctuation">.</span>count<span class="token punctuation">(</span><span class="token string">'1'</span><span class="token punctuation">)</span>
</code></pre>

---
layout: splash
title: Leaderboard
permalink: /leaderboard/
classes:
    - landing
    - dark-theme
---

# **LeaderBoard - AnesBench**

The following leaderboard presents the performance of over fifty different models on AnesBench and AMCQA. The "Average" refers to the mean score across both AnesBench and AMCQA.

<script src="https://cdn.jsdelivr.net/gh/tofsjonas/sortable/sortable.min.js"></script>
<script>
  document.addEventListener('DOMContentLoaded', function () {
    const table = document.querySelector('table.sortable');
    if (!table) return;

    const ths = table.querySelectorAll('thead th');
    let targetIndex = -1;

    // 寻找“Average”所在的列索引
    ths.forEach((th, index) => {
      const text = th.innerText.trim().toLowerCase();
      if (text.includes("average")) {
        targetIndex = index;
      }
    });

    if (targetIndex !== -1) {
      const th = ths[targetIndex];

      // 模拟两次点击，使其变为降序
      setTimeout(() => {
        th.click(); // 第一次：升序
        th.click(); // 第二次：降序
      }, 0); // 等待 DOM 初始化完毕后执行
    }
  });
</script>

<!-- This will add arrows, as well as support for .no-sort and .indicator-left -->
<link href="https://cdn.jsdelivr.net/gh/tofsjonas/sortable@latest/sortable-base.min.css" rel="stylesheet" />

<!-- This will make it look like the tables in the example, with arrows, striped rows etc. -->
<link href="https://cdn.jsdelivr.net/gh/tofsjonas/sortable@latest/sortable.min.css" rel="stylesheet" />

<style>
    .sortable thead th {
        text-align: center;
        vertical-align: middle;
        position: relative;
        white-space: normal;
        padding-right: 30px;
      }
      
      .sortable thead th span.header-text {
        display: inline-block;
        text-align: center;
        line-height: 1.2;
      }
      
      .sortable thead th::after {
        position: absolute;
        right: 8px;
        top: 50%;
        transform: translateY(-50%);
        display: inline-block;
      }
      .sortable tbody td {
        text-align: center;
        vertical-align: middle;
        position: relative;
        white-space: normal;
      }
      .sortable {
        width: 100%;
        max-width: 100%;
        min-width: 100%;
        display: table;
        table-layout: fixed;
        overflow: hidden;
      }

  </style>

<body>

<table class="sortable">
  <thead>
    <tr>
      <th>LLM</th>
      <th>AnesBench<br>system1</th>
      <th>AnesBench<br>system1.x</th>
      <th>AnesBench<br>system2</th>
      <th>AnesBench<br>overall</th>
      <th>AMCQA<br>system1</th>
      <th>AMCQA<br>system1.x</th>
      <th>AMCQA<br>system2</th>
      <th>AMCQA<br>overall</th>
      <th aria-sort="descending">Average</th>
    </tr>
  </thead>
  <tbody>
<tr>
      <td>Qwen3-0.6B</td>
      <td>0.39</td>
      <td>0.31</td>
      <td>0.26</td>
      <td>0.36</td>
      <td>0.37</td>
      <td>0.35</td>
      <td>0.31</td>
      <td>0.37</td>
      <td>0.36</td>
</tr>
<tr>
      <td>gemma-3-1b-it</td>
      <td>0.33</td>
      <td>0.26</td>
      <td>0.21</td>
      <td>0.3</td>
      <td>0.26</td>
      <td>0.25</td>
      <td>0.21</td>
      <td>0.26</td>
      <td>0.28</td>
</tr>
<tr>
      <td>DeepSeek-R1-Distill-Qwen-1.5B</td>
      <td>0.32</td>
      <td>0.28</td>
      <td>0.27</td>
      <td>0.31</td>
      <td>0.26</td>
      <td>0.26</td>
      <td>0.22</td>
      <td>0.26</td>
      <td>0.28</td>
</tr>
<tr>
      <td>Qwen3-1.7B</td>
      <td>0.48</td>
      <td>0.37</td>
      <td>0.3</td>
      <td>0.44</td>
      <td>0.54</td>
      <td>0.5</td>
      <td>0.44</td>
      <td>0.53</td>
      <td>0.48</td>
</tr>
<tr>
      <td>Qwen3-4B</td>
      <td>0.6</td>
      <td>0.46</td>
      <td>0.34</td>
      <td>0.54</td>
      <td>0.54</td>
      <td>0.48</td>
      <td>0.48</td>
      <td>0.53</td>
      <td>0.53</td>
</tr>
<tr>
      <td>gemma-3-4b-it</td>
      <td>0.46</td>
      <td>0.36</td>
      <td>0.35</td>
      <td>0.42</td>
      <td>0.43</td>
      <td>0.41</td>
      <td>0.37</td>
      <td>0.43</td>
      <td>0.42</td>
</tr>
<tr>
      <td>chatglm3-6b</td>
      <td>0.37</td>
      <td>0.28</td>
      <td>0.25</td>
      <td>0.34</td>
      <td>0.36</td>
      <td>0.36</td>
      <td>0.34</td>
      <td>0.36</td>
      <td>0.35</td>
</tr>
<tr>
      <td>Qwen2.5-7B-Instruct</td>
      <td>0.56</td>
      <td>0.44</td>
      <td>0.36</td>
      <td>0.52</td>
      <td>0.68</td>
      <td>0.63</td>
      <td>0.58</td>
      <td>0.67</td>
      <td>0.59</td>
</tr>
<tr>
      <td>HuatuoGPT-o1-7B</td>
      <td>0.56</td>
      <td>0.45</td>
      <td>0.38</td>
      <td>0.52</td>
      <td>0.71</td>
      <td>0.65</td>
      <td>0.63</td>
      <td>0.7</td>
      <td>0.61</td>
</tr>
<tr>
      <td>Baichuan2-7B-Chat</td>
      <td>0.39</td>
      <td>0.31</td>
      <td>0.3</td>
      <td>0.37</td>
      <td>0.44</td>
      <td>0.41</td>
      <td>0.41</td>
      <td>0.43</td>
      <td>0.4</td>
</tr>
<tr>
      <td>BioMistral-7B</td>
      <td>0.43</td>
      <td>0.3</td>
      <td>0.32</td>
      <td>0.39</td>
      <td>0.26</td>
      <td>0.25</td>
      <td>0.28</td>
      <td>0.26</td>
      <td>0.32</td>
</tr>
<tr>
      <td>DeepSeek-R1-Distill-Qwen-7B</td>
      <td>0.4</td>
      <td>0.34</td>
      <td>0.28</td>
      <td>0.38</td>
      <td>0.33</td>
      <td>0.32</td>
      <td>0.34</td>
      <td>0.33</td>
      <td>0.35</td>
</tr>
<tr>
      <td>Qwen3-8B</td>
      <td>0.65</td>
      <td>0.5</td>
      <td>0.4</td>
      <td>0.6</td>
      <td>0.68</td>
      <td>0.53</td>
      <td>0.5</td>
      <td>0.65</td>
      <td>0.62</td>
</tr>
<tr>
      <td>Meta-Llama-3-8B-Instruct</td>
      <td>0.54</td>
      <td>0.42</td>
      <td>0.39</td>
      <td>0.5</td>
      <td>0.49</td>
      <td>0.47</td>
      <td>0.47</td>
      <td>0.49</td>
      <td>0.49</td>
</tr>
<tr>
      <td>Llama-3.1-8B-Instruct</td>
      <td>0.58</td>
      <td>0.45</td>
      <td>0.36</td>
      <td>0.53</td>
      <td>0.53</td>
      <td>0.53</td>
      <td>0.55</td>
      <td>0.53</td>
      <td>0.53</td>
</tr>
<tr>
      <td>Llama-3.1-8B-UltraMedical</td>
      <td>0.63</td>
      <td>0.47</td>
      <td>0.41</td>
      <td>0.57</td>
      <td>0.54</td>
      <td>0.52</td>
      <td>0.5</td>
      <td>0.54</td>
      <td>0.56</td>
</tr>
<tr>
      <td>HuatuoGPT-o1-8B</td>
      <td>0.58</td>
      <td>0.46</td>
      <td>0.39</td>
      <td>0.53</td>
      <td>0.57</td>
      <td>0.53</td>
      <td>0.57</td>
      <td>0.56</td>
      <td>0.55</td>
</tr>
<tr>
      <td>Llama3-OpenBioLLM-8B</td>
      <td>0.44</td>
      <td>0.35</td>
      <td>0.3</td>
      <td>0.41</td>
      <td>0.26</td>
      <td>0.25</td>
      <td>0.19</td>
      <td>0.25</td>
      <td>0.33</td>
</tr>
<tr>
      <td>FineMedLM</td>
      <td>0.4</td>
      <td>0.35</td>
      <td>0.27</td>
      <td>0.38</td>
      <td>0.3</td>
      <td>0.34</td>
      <td>0.38</td>
      <td>0.31</td>
      <td>0.34</td>
</tr>
<tr>
      <td>FineMedLM-o1</td>
      <td>0.43</td>
      <td>0.34</td>
      <td>0.26</td>
      <td>0.39</td>
      <td>0.34</td>
      <td>0.38</td>
      <td>0.4</td>
      <td>0.35</td>
      <td>0.37</td>
</tr>
<tr>
      <td>Bio-Medical-Llama-3-8B</td>
      <td>0.53</td>
      <td>0.41</td>
      <td>0.38</td>
      <td>0.49</td>
      <td>0.48</td>
      <td>0.47</td>
      <td>0.49</td>
      <td>0.48</td>
      <td>0.48</td>
</tr>
<tr>
      <td>internlm3-8b-instruct</td>
      <td>0.6</td>
      <td>0.43</td>
      <td>0.4</td>
      <td>0.54</td>
      <td>0.85</td>
      <td>0.76</td>
      <td>0.77</td>
      <td>0.84</td>
      <td>0.69</td>
</tr>
<tr>
      <td>glm-4-9b-chat</td>
      <td>0.48</td>
      <td>0.36</td>
      <td>0.36</td>
      <td>0.44</td>
      <td>0.61</td>
      <td>0.6</td>
      <td>0.56</td>
      <td>0.61</td>
      <td>0.53</td>
</tr>
<tr>
      <td>gemma-2-9b-it</td>
      <td>0.53</td>
      <td>0.4</td>
      <td>0.36</td>
      <td>0.49</td>
      <td>0.54</td>
      <td>0.49</td>
      <td>0.41</td>
      <td>0.52</td>
      <td>0.51</td>
</tr>
<tr>
      <td>gemma-3-12b-it</td>
      <td>0.56</td>
      <td>0.46</td>
      <td>0.36</td>
      <td>0.52</td>
      <td>0.59</td>
      <td>0.55</td>
      <td>0.51</td>
      <td>0.58</td>
      <td>0.55</td>
</tr>
<tr>
      <td>Baichuan2-13B-Chat</td>
      <td>0.42</td>
      <td>0.31</td>
      <td>0.34</td>
      <td>0.39</td>
      <td>0.48</td>
      <td>0.47</td>
      <td>0.46</td>
      <td>0.48</td>
      <td>0.43</td>
</tr>
<tr>
      <td>phi-4</td>
      <td>0.69</td>
      <td>0.57</td>
      <td>0.41</td>
      <td>0.64</td>
      <td>0.57</td>
      <td>0.57</td>
      <td>0.56</td>
      <td>0.57</td>
      <td>0.6</td>
</tr>
<tr>
      <td>DeepSeek-R1-Distill-Qwen-14B</td>
      <td>0.64</td>
      <td>0.51</td>
      <td>0.4</td>
      <td>0.59</td>
      <td>0.62</td>
      <td>0.66</td>
      <td>0.61</td>
      <td>0.63</td>
      <td>0.61</td>
</tr>
<tr>
      <td>Qwen2.5-14B-Instruct</td>
      <td>0.61</td>
      <td>0.52</td>
      <td>0.41</td>
      <td>0.57</td>
      <td>0.74</td>
      <td>0.7</td>
      <td>0.62</td>
      <td>0.73</td>
      <td>0.65</td>
</tr>
<tr>
      <td>Qwen3-14B</td>
      <td>0.7</td>
      <td>0.57</td>
      <td>0.45</td>
      <td>0.65</td>
      <td>0.77</td>
      <td>0.72</td>
      <td>0.68</td>
      <td>0.76</td>
      <td>0.7</td>
</tr>
<tr>
      <td>gemma-3-27b-it</td>
      <td>0.63</td>
      <td>0.52</td>
      <td>0.4</td>
      <td>0.58</td>
      <td>0.65</td>
      <td>0.62</td>
      <td>0.62</td>
      <td>0.65</td>
      <td>0.61</td>
</tr>
<tr>
      <td>gemma-2-27b-it</td>
      <td>0.6</td>
      <td>0.43</td>
      <td>0.36</td>
      <td>0.54</td>
      <td>0.57</td>
      <td>0.52</td>
      <td>0.48</td>
      <td>0.56</td>
      <td>0.55</td>
</tr>
<tr>
      <td>Qwen3-30B-A3B</td>
      <td>0.73</td>
      <td>0.6</td>
      <td>0.48</td>
      <td>0.68</td>
      <td>0.73</td>
      <td>0.71</td>
      <td>0.7</td>
      <td>0.73</td>
      <td>0.7</td>
</tr>
<tr>
      <td>Qwen3-32B</td>
      <td>0.72</td>
      <td>0.64</td>
      <td>0.48</td>
      <td>0.68</td>
      <td>0.8</td>
      <td>0.77</td>
      <td>0.73</td>
      <td>0.8</td>
      <td>0.74</td>
</tr>
<tr>
      <td>DeepSeek-R1-Distill-Qwen-32B</td>
      <td>0.67</td>
      <td>0.56</td>
      <td>0.45</td>
      <td>0.63</td>
      <td>0.66</td>
      <td>0.71</td>
      <td>0.65</td>
      <td>0.67</td>
      <td>0.65</td>
</tr>
<tr>
      <td>Qwen2.5-32B-Instruct</td>
      <td>0.65</td>
      <td>0.55</td>
      <td>0.44</td>
      <td>0.61</td>
      <td>0.77</td>
      <td>0.73</td>
      <td>0.69</td>
      <td>0.76</td>
      <td>0.68</td>
</tr>
<tr>
      <td>QwQ-32B-Preview</td>
      <td>0.69</td>
      <td>0.58</td>
      <td>0.44</td>
      <td>0.64</td>
      <td>0.74</td>
      <td>0.7</td>
      <td>0.68</td>
      <td>0.73</td>
      <td>0.68</td>
</tr>
<tr>
      <td>Yi-1.5-34B-Chat</td>
      <td>0.54</td>
      <td>0.44</td>
      <td>0.35</td>
      <td>0.5</td>
      <td>0.65</td>
      <td>0.64</td>
      <td>0.64</td>
      <td>0.65</td>
      <td>0.57</td>
</tr>
<tr>
      <td>Llama-3.3-70B-Instruct</td>
      <td>0.74</td>
      <td>0.63</td>
      <td>0.51</td>
      <td>0.7</td>
      <td>0.69</td>
      <td>0.66</td>
      <td>0.63</td>
      <td>0.68</td>
      <td>0.69</td>
</tr>
<tr>
      <td>Llama-3-70B-UltraMedical</td>
      <td>0.73</td>
      <td>0.6</td>
      <td>0.47</td>
      <td>0.68</td>
      <td>0.72</td>
      <td>0.68</td>
      <td>0.62</td>
      <td>0.71</td>
      <td>0.69</td>
</tr>
<tr>
      <td>Llama3-OpenBioLLM-70B</td>
      <td>0.68</td>
      <td>0.55</td>
      <td>0.44</td>
      <td>0.63</td>
      <td>0.65</td>
      <td>0.6</td>
      <td>0.6</td>
      <td>0.64</td>
      <td>0.64</td>
</tr>
<tr>
      <td>Citrus1.0-llama-70B</td>
      <td>0.71</td>
      <td>0.6</td>
      <td>0.52</td>
      <td>0.67</td>
      <td>0.71</td>
      <td>0.69</td>
      <td>0.67</td>
      <td>0.71</td>
      <td>0.69</td>
</tr>
<tr>
      <td>HuatuoGPT-o1-70B</td>
      <td>0.7</td>
      <td>0.58</td>
      <td>0.48</td>
      <td>0.65</td>
      <td>0.7</td>
      <td>0.7</td>
      <td>0.64</td>
      <td>0.7</td>
      <td>0.68</td>
</tr>
<tr>
      <td>DeepSeek-R1-Distill-Llama-70B</td>
      <td>0.77</td>
      <td>0.68</td>
      <td>0.56</td>
      <td>0.73</td>
      <td>0.64</td>
      <td>0.64</td>
      <td>0.59</td>
      <td>0.64</td>
      <td>0.68</td>
</tr>
<tr>
      <td>HuatuoGPT-o1-72B</td>
      <td>0.71</td>
      <td>0.61</td>
      <td>0.48</td>
      <td>0.67</td>
      <td>0.82</td>
      <td>0.78</td>
      <td>0.78</td>
      <td>0.81</td>
      <td>0.74</td>
</tr>
<tr>
      <td>Qwen2.5-72B-Instruct</td>
      <td>0.72</td>
      <td>0.6</td>
      <td>0.48</td>
      <td>0.67</td>
      <td>0.82</td>
      <td>0.77</td>
      <td>0.76</td>
      <td>0.81</td>
      <td>0.74</td>
</tr>
<tr>
      <td>Qwen3-235B-A22B</td>
      <td>0.78</td>
      <td>0.67</td>
      <td>0.57</td>
      <td>0.74</td>
      <td>0.76</td>
      <td>0.73</td>
      <td>0.69</td>
      <td>0.75</td>
      <td>0.74</td>
</tr>
<tr>
      <td>Llama-4-Scout-17B-16E-Instruct</td>
      <td>0.77</td>
      <td>0.66</td>
      <td>0.55</td>
      <td>0.72</td>
      <td>0.8</td>
      <td>0.73</td>
      <td>0.68</td>
      <td>0.78</td>
      <td>0.75</td>
</tr>
<tr>
      <td>deepseek-v3</td>
      <td>0.77</td>
      <td>0.69</td>
      <td>0.55</td>
      <td>0.73</td>
      <td>0.79</td>
      <td>0.77</td>
      <td>0.7</td>
      <td>0.78</td>
      <td>0.76</td>
</tr>
<tr>
      <td>deepseek-r1</td>
      <td>0.85</td>
      <td>0.78</td>
      <td>0.7</td>
      <td>0.82</td>
      <td>0.88</td>
      <td>0.85</td>
      <td>0.81</td>
      <td>0.87</td>
      <td>0.85</td>
</tr>
<tr>
      <td>gpt-4o</td>
      <td>0.81</td>
      <td>0.72</td>
      <td>0.59</td>
      <td>0.77</td>
      <td>0.78</td>
      <td>0.77</td>
      <td>0.68</td>
      <td>0.78</td>
      <td>0.77</td>
</tr>
  </tbody>
</table>
  
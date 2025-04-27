# Omkar-UNICEF
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml" lang="en" xml:lang="en"><head>

<meta charset="utf-8">
<meta name="generator" content="quarto-1.6.42">

<meta name="viewport" content="width=device-width, initial-scale=1.0, user-scalable=yes">


<title>unicef1</title>
<style>
code{white-space: pre-wrap;}
span.smallcaps{font-variant: small-caps;}
div.columns{display: flex; gap: min(4vw, 1.5em);}
div.column{flex: auto; overflow-x: auto;}
div.hanging-indent{margin-left: 1.5em; text-indent: -1.5em;}
ul.task-list{list-style: none;}
ul.task-list li input[type="checkbox"] {
  width: 0.8em;
  margin: 0 0.8em 0.2em -1em; /* quarto-specific, see https://github.com/quarto-dev/quarto-cli/issues/4556 */ 
  vertical-align: middle;
}
/* CSS for syntax highlighting */
pre > code.sourceCode { white-space: pre; position: relative; }
pre > code.sourceCode > span { line-height: 1.25; }
pre > code.sourceCode > span:empty { height: 1.2em; }
.sourceCode { overflow: visible; }
code.sourceCode > span { color: inherit; text-decoration: inherit; }
div.sourceCode { margin: 1em 0; }
pre.sourceCode { margin: 0; }
@media screen {
div.sourceCode { overflow: auto; }
}
@media print {
pre > code.sourceCode { white-space: pre-wrap; }
pre > code.sourceCode > span { display: inline-block; text-indent: -5em; padding-left: 5em; }
}
pre.numberSource code
  { counter-reset: source-line 0; }
pre.numberSource code > span
  { position: relative; left: -4em; counter-increment: source-line; }
pre.numberSource code > span > a:first-child::before
  { content: counter(source-line);
    position: relative; left: -1em; text-align: right; vertical-align: baseline;
    border: none; display: inline-block;
    -webkit-touch-callout: none; -webkit-user-select: none;
    -khtml-user-select: none; -moz-user-select: none;
    -ms-user-select: none; user-select: none;
    padding: 0 4px; width: 4em;
  }
pre.numberSource { margin-left: 3em;  padding-left: 4px; }
div.sourceCode
  {   }
@media screen {
pre > code.sourceCode > span > a:first-child::before { text-decoration: underline; }
}
</style>


<script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.5.1/jquery.min.js" integrity="sha512-bLT0Qm9VnAYZDflyKcBaQ2gg0hSYNQrJ8RilYldYQ1FxQYoCLtUjuuRuZo+fjqhx/qtq/1itJ0C2ejDxltZVFg==" crossorigin="anonymous"></script><script src="unicef1_files/libs/clipboard/clipboard.min.js"></script>
<script src="unicef1_files/libs/quarto-html/quarto.js"></script>
<script src="unicef1_files/libs/quarto-html/popper.min.js"></script>
<script src="unicef1_files/libs/quarto-html/tippy.umd.min.js"></script>
<script src="unicef1_files/libs/quarto-html/anchor.min.js"></script>
<link href="unicef1_files/libs/quarto-html/tippy.css" rel="stylesheet">
<link href="unicef1_files/libs/quarto-html/quarto-syntax-highlighting-2f5df379a58b258e96c21c0638c20c03.css" rel="stylesheet" id="quarto-text-highlighting-styles">
<script src="unicef1_files/libs/bootstrap/bootstrap.min.js"></script>
<link href="unicef1_files/libs/bootstrap/bootstrap-icons.css" rel="stylesheet">
<link href="unicef1_files/libs/bootstrap/bootstrap-133db686e27fe4e6c9e25417b3c932d2.min.css" rel="stylesheet" append-hash="true" id="quarto-bootstrap" data-mode="light">
<script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.3.6/require.min.js" integrity="sha512-c3Nl8+7g4LMSTdrm621y7kf9v3SDPnhxLNhcjFJbKECVnmZHTdo+IRO05sNLTH/D3vA6u1X32ehoLC7WFVdheg==" crossorigin="anonymous"></script>

<script type="application/javascript">define('jquery', [],function() {return window.jQuery;})</script>


</head>

<body class="fullcontent">

<div id="quarto-content" class="page-columns page-rows-contents page-layout-article">

<main class="content" id="quarto-document-content">




<div id="cell-0" class="cell" data-executioninfo="{&quot;status&quot;:&quot;ok&quot;,&quot;timestamp&quot;:1745761052050,&quot;user_tz&quot;:-60,&quot;elapsed&quot;:1389,&quot;user&quot;:{&quot;displayName&quot;:&quot;Omkar Mamidwar&quot;,&quot;userId&quot;:&quot;12811350756920516353&quot;}}" data-execution_count="1">
<div class="sourceCode cell-code" id="cb1"><pre class="sourceCode python code-with-copy"><code class="sourceCode python"><span id="cb1-1"><a href="#cb1-1" aria-hidden="true" tabindex="-1"></a><span class="im">import</span> pandas <span class="im">as</span> pd</span>
<span id="cb1-2"><a href="#cb1-2" aria-hidden="true" tabindex="-1"></a><span class="im">import</span> plotnine <span class="im">as</span> pn</span>
<span id="cb1-3"><a href="#cb1-3" aria-hidden="true" tabindex="-1"></a><span class="im">import</span> geopandas <span class="im">as</span> gpd</span>
<span id="cb1-4"><a href="#cb1-4" aria-hidden="true" tabindex="-1"></a><span class="im">import</span> matplotlib.pyplot <span class="im">as</span> plt</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
</div>
<div id="cell-1" class="cell" data-executioninfo="{&quot;status&quot;:&quot;ok&quot;,&quot;timestamp&quot;:1745761069623,&quot;user_tz&quot;:-60,&quot;elapsed&quot;:50,&quot;user&quot;:{&quot;displayName&quot;:&quot;Omkar Mamidwar&quot;,&quot;userId&quot;:&quot;12811350756920516353&quot;}}" data-execution_count="2">
<div class="sourceCode cell-code" id="cb2"><pre class="sourceCode python code-with-copy"><code class="sourceCode python"><span id="cb2-1"><a href="#cb2-1" aria-hidden="true" tabindex="-1"></a>indicator1 <span class="op">=</span> pd.read_csv(<span class="st">"unicef_indicator_1.csv"</span>)</span>
<span id="cb2-2"><a href="#cb2-2" aria-hidden="true" tabindex="-1"></a>indicator2 <span class="op">=</span> pd.read_csv(<span class="st">"unicef_indicator_2.csv"</span>)</span>
<span id="cb2-3"><a href="#cb2-3" aria-hidden="true" tabindex="-1"></a>metadata <span class="op">=</span> pd.read_csv(<span class="st">"unicef_metadata.csv"</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
</div>
<div id="cell-2" class="cell" data-executioninfo="{&quot;status&quot;:&quot;ok&quot;,&quot;timestamp&quot;:1745761079679,&quot;user_tz&quot;:-60,&quot;elapsed&quot;:99,&quot;user&quot;:{&quot;displayName&quot;:&quot;Omkar Mamidwar&quot;,&quot;userId&quot;:&quot;12811350756920516353&quot;}}" data-outputid="547c6c7d-8371-42bf-feb7-b4c50efbd6be" data-execution_count="3">
<div class="sourceCode cell-code" id="cb3"><pre class="sourceCode python code-with-copy"><code class="sourceCode python"><span id="cb3-1"><a href="#cb3-1" aria-hidden="true" tabindex="-1"></a>indicator1.head()</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-display" data-execution_count="3">

  <div id="df-3cd8dd9c-2140-4db4-9f6b-22a1a06a157c" class="colab-df-container">
    <div>


<table class="dataframe caption-top table table-sm table-striped small" data-quarto-postprocess="true" data-border="1">
<thead>
<tr class="header">
<th data-quarto-table-cell-role="th"></th>
<th data-quarto-table-cell-role="th">country</th>
<th data-quarto-table-cell-role="th">alpha_2_code</th>
<th data-quarto-table-cell-role="th">alpha_3_code</th>
<th data-quarto-table-cell-role="th">numeric_code</th>
<th data-quarto-table-cell-role="th">indicator</th>
<th data-quarto-table-cell-role="th">time_period</th>
<th data-quarto-table-cell-role="th">obs_value</th>
<th data-quarto-table-cell-role="th">sex</th>
<th data-quarto-table-cell-role="th">unit_multiplier</th>
<th data-quarto-table-cell-role="th">unit_of_measure</th>
<th data-quarto-table-cell-role="th">observation_status</th>
<th data-quarto-table-cell-role="th">observation_confidentaility</th>
<th data-quarto-table-cell-role="th">time_period_activity_related_to_when_the_data_are_collected</th>
<th data-quarto-table-cell-role="th">current_age</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td data-quarto-table-cell-role="th">0</td>
<td>Afghanistan</td>
<td>AF</td>
<td>AFG</td>
<td>4</td>
<td>Maternal deaths (estimated)</td>
<td>2000</td>
<td>13407.6</td>
<td>Total</td>
<td>Units</td>
<td>%</td>
<td>Modelled</td>
<td>Free</td>
<td>NaN</td>
<td>Total</td>
</tr>
<tr class="even">
<td data-quarto-table-cell-role="th">1</td>
<td>Afghanistan</td>
<td>AF</td>
<td>AFG</td>
<td>4</td>
<td>Maternal deaths (estimated)</td>
<td>2001</td>
<td>12339.5</td>
<td>Total</td>
<td>Units</td>
<td>%</td>
<td>Modelled</td>
<td>Free</td>
<td>NaN</td>
<td>Total</td>
</tr>
<tr class="odd">
<td data-quarto-table-cell-role="th">2</td>
<td>Afghanistan</td>
<td>AF</td>
<td>AFG</td>
<td>4</td>
<td>Maternal deaths (estimated)</td>
<td>2002</td>
<td>12517.6</td>
<td>Total</td>
<td>Units</td>
<td>%</td>
<td>Modelled</td>
<td>Free</td>
<td>NaN</td>
<td>Total</td>
</tr>
<tr class="even">
<td data-quarto-table-cell-role="th">3</td>
<td>Afghanistan</td>
<td>AF</td>
<td>AFG</td>
<td>4</td>
<td>Maternal deaths (estimated)</td>
<td>2003</td>
<td>12714.4</td>
<td>Total</td>
<td>Units</td>
<td>%</td>
<td>Modelled</td>
<td>Free</td>
<td>NaN</td>
<td>Total</td>
</tr>
<tr class="odd">
<td data-quarto-table-cell-role="th">4</td>
<td>Afghanistan</td>
<td>AF</td>
<td>AFG</td>
<td>4</td>
<td>Maternal deaths (estimated)</td>
<td>2004</td>
<td>12230.3</td>
<td>Total</td>
<td>Units</td>
<td>%</td>
<td>Modelled</td>
<td>Free</td>
<td>NaN</td>
<td>Total</td>
</tr>
</tbody>
</table>

</div>
    <div class="colab-df-buttons">

  <div class="colab-df-container">
    <button class="colab-df-convert" onclick="convertToInteractive('df-3cd8dd9c-2140-4db4-9f6b-22a1a06a157c')" title="Convert this dataframe to an interactive table." style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewbox="0 -960 960 960">
    <path d="M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z"></path>
  </svg>
    </button>

  <style>
    .colab-df-container {
      display:flex;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    .colab-df-buttons div {
      margin-bottom: 4px;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

    <script>
      const buttonEl =
        document.querySelector('#df-3cd8dd9c-2140-4db4-9f6b-22a1a06a157c button.colab-df-convert');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      async function convertToInteractive(key) {
        const element = document.querySelector('#df-3cd8dd9c-2140-4db4-9f6b-22a1a06a157c');
        const dataTable =
          await google.colab.kernel.invokeFunction('convertToInteractive',
                                                    [key], {});
        if (!dataTable) return;

        const docLinkHtml = 'Like what you see? Visit the ' +
          '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
          + ' to learn more about interactive tables.';
        element.innerHTML = '';
        dataTable['output_type'] = 'display_data';
        await google.colab.output.renderOutput(dataTable, element);
        const docLink = document.createElement('div');
        docLink.innerHTML = docLinkHtml;
        element.appendChild(docLink);
      }
    </script>
  </div>


    <div id="df-3e9654b6-c770-4db2-9ce2-38b808e9bf67">
      <button class="colab-df-quickchart" onclick="quickchart('df-3e9654b6-c770-4db2-9ce2-38b808e9bf67')" title="Suggest charts" style="display:none;">

<svg xmlns="http://www.w3.org/2000/svg" height="24px" viewbox="0 0 24 24" width="24px">
    <g>
        <path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zM9 17H7v-7h2v7zm4 0h-2V7h2v10zm4 0h-2v-4h2v4z"></path>
    </g>
</svg>
      </button>

<style>
  .colab-df-quickchart {
      --bg-color: #E8F0FE;
      --fill-color: #1967D2;
      --hover-bg-color: #E2EBFA;
      --hover-fill-color: #174EA6;
      --disabled-fill-color: #AAA;
      --disabled-bg-color: #DDD;
  }

  [theme=dark] .colab-df-quickchart {
      --bg-color: #3B4455;
      --fill-color: #D2E3FC;
      --hover-bg-color: #434B5C;
      --hover-fill-color: #FFFFFF;
      --disabled-bg-color: #3B4455;
      --disabled-fill-color: #666;
  }

  .colab-df-quickchart {
    background-color: var(--bg-color);
    border: none;
    border-radius: 50%;
    cursor: pointer;
    display: none;
    fill: var(--fill-color);
    height: 32px;
    padding: 0;
    width: 32px;
  }

  .colab-df-quickchart:hover {
    background-color: var(--hover-bg-color);
    box-shadow: 0 1px 2px rgba(60, 64, 67, 0.3), 0 1px 3px 1px rgba(60, 64, 67, 0.15);
    fill: var(--button-hover-fill-color);
  }

  .colab-df-quickchart-complete:disabled,
  .colab-df-quickchart-complete:disabled:hover {
    background-color: var(--disabled-bg-color);
    fill: var(--disabled-fill-color);
    box-shadow: none;
  }

  .colab-df-spinner {
    border: 2px solid var(--fill-color);
    border-color: transparent;
    border-bottom-color: var(--fill-color);
    animation:
      spin 1s steps(1) infinite;
  }

  @keyframes spin {
    0% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
      border-left-color: var(--fill-color);
    }
    20% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    30% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
      border-right-color: var(--fill-color);
    }
    40% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    60% {
      border-color: transparent;
      border-right-color: var(--fill-color);
    }
    80% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-bottom-color: var(--fill-color);
    }
    90% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
    }
  }
</style>

      <script>
        async function quickchart(key) {
          const quickchartButtonEl =
            document.querySelector('#' + key + ' button');
          quickchartButtonEl.disabled = true;  // To prevent multiple clicks.
          quickchartButtonEl.classList.add('colab-df-spinner');
          try {
            const charts = await google.colab.kernel.invokeFunction(
                'suggestCharts', [key], {});
          } catch (error) {
            console.error('Error during call to suggestCharts:', error);
          }
          quickchartButtonEl.classList.remove('colab-df-spinner');
          quickchartButtonEl.classList.add('colab-df-quickchart-complete');
        }
        (() => {
          let quickchartButtonEl =
            document.querySelector('#df-3e9654b6-c770-4db2-9ce2-38b808e9bf67 button');
          quickchartButtonEl.style.display =
            google.colab.kernel.accessAllowed ? 'block' : 'none';
        })();
      </script>
    </div>

    </div>
  </div>
</div>
</div>
<div id="cell-3" class="cell" data-executioninfo="{&quot;status&quot;:&quot;ok&quot;,&quot;timestamp&quot;:1745761093965,&quot;user_tz&quot;:-60,&quot;elapsed&quot;:13,&quot;user&quot;:{&quot;displayName&quot;:&quot;Omkar Mamidwar&quot;,&quot;userId&quot;:&quot;12811350756920516353&quot;}}" data-outputid="d8fc7968-1fe9-44e4-fe65-71f41db7ccf8" data-execution_count="4">
<div class="sourceCode cell-code" id="cb4"><pre class="sourceCode python code-with-copy"><code class="sourceCode python"><span id="cb4-1"><a href="#cb4-1" aria-hidden="true" tabindex="-1"></a>indicator1.shape</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-display" data-execution_count="4">
<pre><code>(3885, 14)</code></pre>
</div>
</div>
<div id="cell-4" class="cell" data-executioninfo="{&quot;status&quot;:&quot;ok&quot;,&quot;timestamp&quot;:1745761106642,&quot;user_tz&quot;:-60,&quot;elapsed&quot;:128,&quot;user&quot;:{&quot;displayName&quot;:&quot;Omkar Mamidwar&quot;,&quot;userId&quot;:&quot;12811350756920516353&quot;}}" data-outputid="c2f92510-77e9-466e-f594-db68a5245dd6" data-execution_count="5">
<div class="sourceCode cell-code" id="cb6"><pre class="sourceCode python code-with-copy"><code class="sourceCode python"><span id="cb6-1"><a href="#cb6-1" aria-hidden="true" tabindex="-1"></a>indicator2.head()</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-display" data-execution_count="5">

  <div id="df-5c39941b-2f43-4fc9-a055-c1008168b495" class="colab-df-container">
    <div>


<table class="dataframe caption-top table table-sm table-striped small" data-quarto-postprocess="true" data-border="1">
<thead>
<tr class="header">
<th data-quarto-table-cell-role="th"></th>
<th data-quarto-table-cell-role="th">country</th>
<th data-quarto-table-cell-role="th">alpha_2_code</th>
<th data-quarto-table-cell-role="th">alpha_3_code</th>
<th data-quarto-table-cell-role="th">numeric_code</th>
<th data-quarto-table-cell-role="th">indicator</th>
<th data-quarto-table-cell-role="th">time_period</th>
<th data-quarto-table-cell-role="th">obs_value</th>
<th data-quarto-table-cell-role="th">sex</th>
<th data-quarto-table-cell-role="th">unit_multiplier</th>
<th data-quarto-table-cell-role="th">unit_of_measure</th>
<th data-quarto-table-cell-role="th">observation_status</th>
<th data-quarto-table-cell-role="th">observation_confidentaility</th>
<th data-quarto-table-cell-role="th">time_period_activity_related_to_when_the_data_are_collected</th>
<th data-quarto-table-cell-role="th">current_age</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td data-quarto-table-cell-role="th">0</td>
<td>Afghanistan</td>
<td>AF</td>
<td>AFG</td>
<td>4</td>
<td>Adjusted net attendance rate for children of p...</td>
<td>2015</td>
<td>53.200001</td>
<td>Female</td>
<td>NaN</td>
<td>%</td>
<td>NaN</td>
<td>NaN</td>
<td>NaN</td>
<td>Total</td>
</tr>
<tr class="even">
<td data-quarto-table-cell-role="th">1</td>
<td>Afghanistan</td>
<td>AF</td>
<td>AFG</td>
<td>4</td>
<td>Adjusted net attendance rate for children of p...</td>
<td>2015</td>
<td>73.099998</td>
<td>Male</td>
<td>NaN</td>
<td>%</td>
<td>NaN</td>
<td>NaN</td>
<td>NaN</td>
<td>Total</td>
</tr>
<tr class="odd">
<td data-quarto-table-cell-role="th">2</td>
<td>Afghanistan</td>
<td>AF</td>
<td>AFG</td>
<td>4</td>
<td>Adjusted net attendance rate for children of p...</td>
<td>2015</td>
<td>63.700001</td>
<td>Total</td>
<td>NaN</td>
<td>%</td>
<td>NaN</td>
<td>NaN</td>
<td>NaN</td>
<td>Total</td>
</tr>
<tr class="even">
<td data-quarto-table-cell-role="th">3</td>
<td>Albania</td>
<td>AL</td>
<td>ALB</td>
<td>8</td>
<td>Adjusted net attendance rate for children of p...</td>
<td>2018</td>
<td>91.392990</td>
<td>Female</td>
<td>NaN</td>
<td>%</td>
<td>NaN</td>
<td>NaN</td>
<td>NaN</td>
<td>Total</td>
</tr>
<tr class="odd">
<td data-quarto-table-cell-role="th">4</td>
<td>Albania</td>
<td>AL</td>
<td>ALB</td>
<td>8</td>
<td>Adjusted net attendance rate for children of p...</td>
<td>2018</td>
<td>88.879219</td>
<td>Male</td>
<td>NaN</td>
<td>%</td>
<td>NaN</td>
<td>NaN</td>
<td>NaN</td>
<td>Total</td>
</tr>
</tbody>
</table>

</div>
    <div class="colab-df-buttons">

  <div class="colab-df-container">
    <button class="colab-df-convert" onclick="convertToInteractive('df-5c39941b-2f43-4fc9-a055-c1008168b495')" title="Convert this dataframe to an interactive table." style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewbox="0 -960 960 960">
    <path d="M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z"></path>
  </svg>
    </button>

  <style>
    .colab-df-container {
      display:flex;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    .colab-df-buttons div {
      margin-bottom: 4px;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

    <script>
      const buttonEl =
        document.querySelector('#df-5c39941b-2f43-4fc9-a055-c1008168b495 button.colab-df-convert');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      async function convertToInteractive(key) {
        const element = document.querySelector('#df-5c39941b-2f43-4fc9-a055-c1008168b495');
        const dataTable =
          await google.colab.kernel.invokeFunction('convertToInteractive',
                                                    [key], {});
        if (!dataTable) return;

        const docLinkHtml = 'Like what you see? Visit the ' +
          '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
          + ' to learn more about interactive tables.';
        element.innerHTML = '';
        dataTable['output_type'] = 'display_data';
        await google.colab.output.renderOutput(dataTable, element);
        const docLink = document.createElement('div');
        docLink.innerHTML = docLinkHtml;
        element.appendChild(docLink);
      }
    </script>
  </div>


    <div id="df-f5dcd6e8-01d0-499e-83f1-cc5597612a63">
      <button class="colab-df-quickchart" onclick="quickchart('df-f5dcd6e8-01d0-499e-83f1-cc5597612a63')" title="Suggest charts" style="display:none;">

<svg xmlns="http://www.w3.org/2000/svg" height="24px" viewbox="0 0 24 24" width="24px">
    <g>
        <path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zM9 17H7v-7h2v7zm4 0h-2V7h2v10zm4 0h-2v-4h2v4z"></path>
    </g>
</svg>
      </button>

<style>
  .colab-df-quickchart {
      --bg-color: #E8F0FE;
      --fill-color: #1967D2;
      --hover-bg-color: #E2EBFA;
      --hover-fill-color: #174EA6;
      --disabled-fill-color: #AAA;
      --disabled-bg-color: #DDD;
  }

  [theme=dark] .colab-df-quickchart {
      --bg-color: #3B4455;
      --fill-color: #D2E3FC;
      --hover-bg-color: #434B5C;
      --hover-fill-color: #FFFFFF;
      --disabled-bg-color: #3B4455;
      --disabled-fill-color: #666;
  }

  .colab-df-quickchart {
    background-color: var(--bg-color);
    border: none;
    border-radius: 50%;
    cursor: pointer;
    display: none;
    fill: var(--fill-color);
    height: 32px;
    padding: 0;
    width: 32px;
  }

  .colab-df-quickchart:hover {
    background-color: var(--hover-bg-color);
    box-shadow: 0 1px 2px rgba(60, 64, 67, 0.3), 0 1px 3px 1px rgba(60, 64, 67, 0.15);
    fill: var(--button-hover-fill-color);
  }

  .colab-df-quickchart-complete:disabled,
  .colab-df-quickchart-complete:disabled:hover {
    background-color: var(--disabled-bg-color);
    fill: var(--disabled-fill-color);
    box-shadow: none;
  }

  .colab-df-spinner {
    border: 2px solid var(--fill-color);
    border-color: transparent;
    border-bottom-color: var(--fill-color);
    animation:
      spin 1s steps(1) infinite;
  }

  @keyframes spin {
    0% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
      border-left-color: var(--fill-color);
    }
    20% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    30% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
      border-right-color: var(--fill-color);
    }
    40% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    60% {
      border-color: transparent;
      border-right-color: var(--fill-color);
    }
    80% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-bottom-color: var(--fill-color);
    }
    90% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
    }
  }
</style>

      <script>
        async function quickchart(key) {
          const quickchartButtonEl =
            document.querySelector('#' + key + ' button');
          quickchartButtonEl.disabled = true;  // To prevent multiple clicks.
          quickchartButtonEl.classList.add('colab-df-spinner');
          try {
            const charts = await google.colab.kernel.invokeFunction(
                'suggestCharts', [key], {});
          } catch (error) {
            console.error('Error during call to suggestCharts:', error);
          }
          quickchartButtonEl.classList.remove('colab-df-spinner');
          quickchartButtonEl.classList.add('colab-df-quickchart-complete');
        }
        (() => {
          let quickchartButtonEl =
            document.querySelector('#df-f5dcd6e8-01d0-499e-83f1-cc5597612a63 button');
          quickchartButtonEl.style.display =
            google.colab.kernel.accessAllowed ? 'block' : 'none';
        })();
      </script>
    </div>

    </div>
  </div>
</div>
</div>
<div id="cell-5" class="cell" data-executioninfo="{&quot;status&quot;:&quot;ok&quot;,&quot;timestamp&quot;:1745761124496,&quot;user_tz&quot;:-60,&quot;elapsed&quot;:174,&quot;user&quot;:{&quot;displayName&quot;:&quot;Omkar Mamidwar&quot;,&quot;userId&quot;:&quot;12811350756920516353&quot;}}" data-outputid="9dc4d302-5566-420c-c0ff-a3bb9d0fa260" data-execution_count="6">
<div class="sourceCode cell-code" id="cb7"><pre class="sourceCode python code-with-copy"><code class="sourceCode python"><span id="cb7-1"><a href="#cb7-1" aria-hidden="true" tabindex="-1"></a>metadata.head()</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-display" data-execution_count="6">

  <div id="df-56f77721-3106-49bf-81b4-b7cd36885607" class="colab-df-container">
    <div>


<table class="dataframe caption-top table table-sm table-striped small" data-quarto-postprocess="true" data-border="1">
<thead>
<tr class="header">
<th data-quarto-table-cell-role="th"></th>
<th data-quarto-table-cell-role="th">country</th>
<th data-quarto-table-cell-role="th">alpha_2_code</th>
<th data-quarto-table-cell-role="th">alpha_3_code</th>
<th data-quarto-table-cell-role="th">numeric_code</th>
<th data-quarto-table-cell-role="th">year</th>
<th data-quarto-table-cell-role="th">Population, total</th>
<th data-quarto-table-cell-role="th">GDP per capita (constant 2015 US$)</th>
<th data-quarto-table-cell-role="th">GNI (current US$)</th>
<th data-quarto-table-cell-role="th">Inflation, consumer prices (annual %)</th>
<th data-quarto-table-cell-role="th">Life expectancy at birth, total (years)</th>
<th data-quarto-table-cell-role="th">Military expenditure (% of GDP)</th>
<th data-quarto-table-cell-role="th">Fossil fuel energy consumption (% of total)</th>
<th data-quarto-table-cell-role="th">GDP growth (annual %)</th>
<th data-quarto-table-cell-role="th">Birth rate, crude (per 1,000 people)</th>
<th data-quarto-table-cell-role="th">Hospital beds (per 1,000 people)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td data-quarto-table-cell-role="th">0</td>
<td>Afghanistan</td>
<td>AF</td>
<td>AFG</td>
<td>4</td>
<td>1960</td>
<td>9035043.0</td>
<td>NaN</td>
<td>5.488888e+08</td>
<td>NaN</td>
<td>32.535</td>
<td>NaN</td>
<td>NaN</td>
<td>NaN</td>
<td>50.340</td>
<td>0.170627</td>
</tr>
<tr class="even">
<td data-quarto-table-cell-role="th">1</td>
<td>Afghanistan</td>
<td>AF</td>
<td>AFG</td>
<td>4</td>
<td>1961</td>
<td>9214083.0</td>
<td>NaN</td>
<td>5.600000e+08</td>
<td>NaN</td>
<td>33.068</td>
<td>NaN</td>
<td>NaN</td>
<td>NaN</td>
<td>50.443</td>
<td>NaN</td>
</tr>
<tr class="odd">
<td data-quarto-table-cell-role="th">2</td>
<td>Afghanistan</td>
<td>AF</td>
<td>AFG</td>
<td>4</td>
<td>1962</td>
<td>9404406.0</td>
<td>NaN</td>
<td>5.577778e+08</td>
<td>NaN</td>
<td>33.547</td>
<td>NaN</td>
<td>NaN</td>
<td>NaN</td>
<td>50.570</td>
<td>NaN</td>
</tr>
<tr class="even">
<td data-quarto-table-cell-role="th">3</td>
<td>Afghanistan</td>
<td>AF</td>
<td>AFG</td>
<td>4</td>
<td>1963</td>
<td>9604487.0</td>
<td>NaN</td>
<td>7.666667e+08</td>
<td>NaN</td>
<td>34.016</td>
<td>NaN</td>
<td>NaN</td>
<td>NaN</td>
<td>50.703</td>
<td>NaN</td>
</tr>
<tr class="odd">
<td data-quarto-table-cell-role="th">4</td>
<td>Afghanistan</td>
<td>AF</td>
<td>AFG</td>
<td>4</td>
<td>1964</td>
<td>9814318.0</td>
<td>NaN</td>
<td>8.155556e+08</td>
<td>NaN</td>
<td>34.494</td>
<td>NaN</td>
<td>NaN</td>
<td>NaN</td>
<td>50.831</td>
<td>NaN</td>
</tr>
</tbody>
</table>

</div>
    <div class="colab-df-buttons">

  <div class="colab-df-container">
    <button class="colab-df-convert" onclick="convertToInteractive('df-56f77721-3106-49bf-81b4-b7cd36885607')" title="Convert this dataframe to an interactive table." style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewbox="0 -960 960 960">
    <path d="M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z"></path>
  </svg>
    </button>

  <style>
    .colab-df-container {
      display:flex;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    .colab-df-buttons div {
      margin-bottom: 4px;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

    <script>
      const buttonEl =
        document.querySelector('#df-56f77721-3106-49bf-81b4-b7cd36885607 button.colab-df-convert');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      async function convertToInteractive(key) {
        const element = document.querySelector('#df-56f77721-3106-49bf-81b4-b7cd36885607');
        const dataTable =
          await google.colab.kernel.invokeFunction('convertToInteractive',
                                                    [key], {});
        if (!dataTable) return;

        const docLinkHtml = 'Like what you see? Visit the ' +
          '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
          + ' to learn more about interactive tables.';
        element.innerHTML = '';
        dataTable['output_type'] = 'display_data';
        await google.colab.output.renderOutput(dataTable, element);
        const docLink = document.createElement('div');
        docLink.innerHTML = docLinkHtml;
        element.appendChild(docLink);
      }
    </script>
  </div>


    <div id="df-f43cd7a8-0fb7-43ce-bf5f-78929b6e5824">
      <button class="colab-df-quickchart" onclick="quickchart('df-f43cd7a8-0fb7-43ce-bf5f-78929b6e5824')" title="Suggest charts" style="display:none;">

<svg xmlns="http://www.w3.org/2000/svg" height="24px" viewbox="0 0 24 24" width="24px">
    <g>
        <path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zM9 17H7v-7h2v7zm4 0h-2V7h2v10zm4 0h-2v-4h2v4z"></path>
    </g>
</svg>
      </button>

<style>
  .colab-df-quickchart {
      --bg-color: #E8F0FE;
      --fill-color: #1967D2;
      --hover-bg-color: #E2EBFA;
      --hover-fill-color: #174EA6;
      --disabled-fill-color: #AAA;
      --disabled-bg-color: #DDD;
  }

  [theme=dark] .colab-df-quickchart {
      --bg-color: #3B4455;
      --fill-color: #D2E3FC;
      --hover-bg-color: #434B5C;
      --hover-fill-color: #FFFFFF;
      --disabled-bg-color: #3B4455;
      --disabled-fill-color: #666;
  }

  .colab-df-quickchart {
    background-color: var(--bg-color);
    border: none;
    border-radius: 50%;
    cursor: pointer;
    display: none;
    fill: var(--fill-color);
    height: 32px;
    padding: 0;
    width: 32px;
  }

  .colab-df-quickchart:hover {
    background-color: var(--hover-bg-color);
    box-shadow: 0 1px 2px rgba(60, 64, 67, 0.3), 0 1px 3px 1px rgba(60, 64, 67, 0.15);
    fill: var(--button-hover-fill-color);
  }

  .colab-df-quickchart-complete:disabled,
  .colab-df-quickchart-complete:disabled:hover {
    background-color: var(--disabled-bg-color);
    fill: var(--disabled-fill-color);
    box-shadow: none;
  }

  .colab-df-spinner {
    border: 2px solid var(--fill-color);
    border-color: transparent;
    border-bottom-color: var(--fill-color);
    animation:
      spin 1s steps(1) infinite;
  }

  @keyframes spin {
    0% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
      border-left-color: var(--fill-color);
    }
    20% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    30% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
      border-right-color: var(--fill-color);
    }
    40% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    60% {
      border-color: transparent;
      border-right-color: var(--fill-color);
    }
    80% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-bottom-color: var(--fill-color);
    }
    90% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
    }
  }
</style>

      <script>
        async function quickchart(key) {
          const quickchartButtonEl =
            document.querySelector('#' + key + ' button');
          quickchartButtonEl.disabled = true;  // To prevent multiple clicks.
          quickchartButtonEl.classList.add('colab-df-spinner');
          try {
            const charts = await google.colab.kernel.invokeFunction(
                'suggestCharts', [key], {});
          } catch (error) {
            console.error('Error during call to suggestCharts:', error);
          }
          quickchartButtonEl.classList.remove('colab-df-spinner');
          quickchartButtonEl.classList.add('colab-df-quickchart-complete');
        }
        (() => {
          let quickchartButtonEl =
            document.querySelector('#df-f43cd7a8-0fb7-43ce-bf5f-78929b6e5824 button');
          quickchartButtonEl.style.display =
            google.colab.kernel.accessAllowed ? 'block' : 'none';
        })();
      </script>
    </div>

    </div>
  </div>
</div>
</div>
<div id="cell-6" class="cell" data-executioninfo="{&quot;status&quot;:&quot;ok&quot;,&quot;timestamp&quot;:1745761223667,&quot;user_tz&quot;:-60,&quot;elapsed&quot;:303,&quot;user&quot;:{&quot;displayName&quot;:&quot;Omkar Mamidwar&quot;,&quot;userId&quot;:&quot;12811350756920516353&quot;}}" data-execution_count="7">
<div class="sourceCode cell-code" id="cb8"><pre class="sourceCode python code-with-copy"><code class="sourceCode python"><span id="cb8-1"><a href="#cb8-1" aria-hidden="true" tabindex="-1"></a>combined <span class="op">=</span> pd.merge(indicator1, indicator2, on<span class="op">=</span>[<span class="st">"country"</span>, <span class="st">"time_period"</span>], how<span class="op">=</span><span class="st">"outer"</span>)</span>
<span id="cb8-2"><a href="#cb8-2" aria-hidden="true" tabindex="-1"></a>combined <span class="op">=</span> pd.merge(combined, metadata, on<span class="op">=</span><span class="st">"country"</span>, how<span class="op">=</span><span class="st">"left"</span>)</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
</div>
<div id="cell-7" class="cell" data-executioninfo="{&quot;status&quot;:&quot;ok&quot;,&quot;timestamp&quot;:1745761235026,&quot;user_tz&quot;:-60,&quot;elapsed&quot;:117,&quot;user&quot;:{&quot;displayName&quot;:&quot;Omkar Mamidwar&quot;,&quot;userId&quot;:&quot;12811350756920516353&quot;}}" data-outputid="c521be6f-7a3c-4a57-9e62-68fc4828a843" data-execution_count="8">
<div class="sourceCode cell-code" id="cb9"><pre class="sourceCode python code-with-copy"><code class="sourceCode python"><span id="cb9-1"><a href="#cb9-1" aria-hidden="true" tabindex="-1"></a>combined.head()</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-display" data-execution_count="8">

  <div id="df-b4fca39b-8a9c-4452-b284-dd7f3ae33101" class="colab-df-container">
    <div>


<table class="dataframe caption-top table table-sm table-striped small" data-quarto-postprocess="true" data-border="1">
<thead>
<tr class="header">
<th data-quarto-table-cell-role="th"></th>
<th data-quarto-table-cell-role="th">country</th>
<th data-quarto-table-cell-role="th">alpha_2_code_x</th>
<th data-quarto-table-cell-role="th">alpha_3_code_x</th>
<th data-quarto-table-cell-role="th">numeric_code_x</th>
<th data-quarto-table-cell-role="th">indicator_x</th>
<th data-quarto-table-cell-role="th">time_period</th>
<th data-quarto-table-cell-role="th">obs_value_x</th>
<th data-quarto-table-cell-role="th">sex_x</th>
<th data-quarto-table-cell-role="th">unit_multiplier_x</th>
<th data-quarto-table-cell-role="th">unit_of_measure_x</th>
<th data-quarto-table-cell-role="th">...</th>
<th data-quarto-table-cell-role="th">Population, total</th>
<th data-quarto-table-cell-role="th">GDP per capita (constant 2015 US$)</th>
<th data-quarto-table-cell-role="th">GNI (current US$)</th>
<th data-quarto-table-cell-role="th">Inflation, consumer prices (annual %)</th>
<th data-quarto-table-cell-role="th">Life expectancy at birth, total (years)</th>
<th data-quarto-table-cell-role="th">Military expenditure (% of GDP)</th>
<th data-quarto-table-cell-role="th">Fossil fuel energy consumption (% of total)</th>
<th data-quarto-table-cell-role="th">GDP growth (annual %)</th>
<th data-quarto-table-cell-role="th">Birth rate, crude (per 1,000 people)</th>
<th data-quarto-table-cell-role="th">Hospital beds (per 1,000 people)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td data-quarto-table-cell-role="th">0</td>
<td>Afghanistan</td>
<td>AF</td>
<td>AFG</td>
<td>4.0</td>
<td>Maternal deaths (estimated)</td>
<td>2000</td>
<td>13407.6</td>
<td>Total</td>
<td>Units</td>
<td>%</td>
<td>...</td>
<td>9035043.0</td>
<td>NaN</td>
<td>5.488888e+08</td>
<td>NaN</td>
<td>32.535</td>
<td>NaN</td>
<td>NaN</td>
<td>NaN</td>
<td>50.340</td>
<td>0.170627</td>
</tr>
<tr class="even">
<td data-quarto-table-cell-role="th">1</td>
<td>Afghanistan</td>
<td>AF</td>
<td>AFG</td>
<td>4.0</td>
<td>Maternal deaths (estimated)</td>
<td>2000</td>
<td>13407.6</td>
<td>Total</td>
<td>Units</td>
<td>%</td>
<td>...</td>
<td>9214083.0</td>
<td>NaN</td>
<td>5.600000e+08</td>
<td>NaN</td>
<td>33.068</td>
<td>NaN</td>
<td>NaN</td>
<td>NaN</td>
<td>50.443</td>
<td>NaN</td>
</tr>
<tr class="odd">
<td data-quarto-table-cell-role="th">2</td>
<td>Afghanistan</td>
<td>AF</td>
<td>AFG</td>
<td>4.0</td>
<td>Maternal deaths (estimated)</td>
<td>2000</td>
<td>13407.6</td>
<td>Total</td>
<td>Units</td>
<td>%</td>
<td>...</td>
<td>9404406.0</td>
<td>NaN</td>
<td>5.577778e+08</td>
<td>NaN</td>
<td>33.547</td>
<td>NaN</td>
<td>NaN</td>
<td>NaN</td>
<td>50.570</td>
<td>NaN</td>
</tr>
<tr class="even">
<td data-quarto-table-cell-role="th">3</td>
<td>Afghanistan</td>
<td>AF</td>
<td>AFG</td>
<td>4.0</td>
<td>Maternal deaths (estimated)</td>
<td>2000</td>
<td>13407.6</td>
<td>Total</td>
<td>Units</td>
<td>%</td>
<td>...</td>
<td>9604487.0</td>
<td>NaN</td>
<td>7.666667e+08</td>
<td>NaN</td>
<td>34.016</td>
<td>NaN</td>
<td>NaN</td>
<td>NaN</td>
<td>50.703</td>
<td>NaN</td>
</tr>
<tr class="odd">
<td data-quarto-table-cell-role="th">4</td>
<td>Afghanistan</td>
<td>AF</td>
<td>AFG</td>
<td>4.0</td>
<td>Maternal deaths (estimated)</td>
<td>2000</td>
<td>13407.6</td>
<td>Total</td>
<td>Units</td>
<td>%</td>
<td>...</td>
<td>9814318.0</td>
<td>NaN</td>
<td>8.155556e+08</td>
<td>NaN</td>
<td>34.494</td>
<td>NaN</td>
<td>NaN</td>
<td>NaN</td>
<td>50.831</td>
<td>NaN</td>
</tr>
</tbody>
</table>

<p>5 rows × 40 columns</p>
</div>
    <div class="colab-df-buttons">

  <div class="colab-df-container">
    <button class="colab-df-convert" onclick="convertToInteractive('df-b4fca39b-8a9c-4452-b284-dd7f3ae33101')" title="Convert this dataframe to an interactive table." style="display:none;">

  <svg xmlns="http://www.w3.org/2000/svg" height="24px" viewbox="0 -960 960 960">
    <path d="M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z"></path>
  </svg>
    </button>

  <style>
    .colab-df-container {
      display:flex;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    .colab-df-buttons div {
      margin-bottom: 4px;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>

    <script>
      const buttonEl =
        document.querySelector('#df-b4fca39b-8a9c-4452-b284-dd7f3ae33101 button.colab-df-convert');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      async function convertToInteractive(key) {
        const element = document.querySelector('#df-b4fca39b-8a9c-4452-b284-dd7f3ae33101');
        const dataTable =
          await google.colab.kernel.invokeFunction('convertToInteractive',
                                                    [key], {});
        if (!dataTable) return;

        const docLinkHtml = 'Like what you see? Visit the ' +
          '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
          + ' to learn more about interactive tables.';
        element.innerHTML = '';
        dataTable['output_type'] = 'display_data';
        await google.colab.output.renderOutput(dataTable, element);
        const docLink = document.createElement('div');
        docLink.innerHTML = docLinkHtml;
        element.appendChild(docLink);
      }
    </script>
  </div>


    <div id="df-605dc61f-5b70-43ac-8d38-d4baab0d7d8d">
      <button class="colab-df-quickchart" onclick="quickchart('df-605dc61f-5b70-43ac-8d38-d4baab0d7d8d')" title="Suggest charts" style="display:none;">

<svg xmlns="http://www.w3.org/2000/svg" height="24px" viewbox="0 0 24 24" width="24px">
    <g>
        <path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zM9 17H7v-7h2v7zm4 0h-2V7h2v10zm4 0h-2v-4h2v4z"></path>
    </g>
</svg>
      </button>

<style>
  .colab-df-quickchart {
      --bg-color: #E8F0FE;
      --fill-color: #1967D2;
      --hover-bg-color: #E2EBFA;
      --hover-fill-color: #174EA6;
      --disabled-fill-color: #AAA;
      --disabled-bg-color: #DDD;
  }

  [theme=dark] .colab-df-quickchart {
      --bg-color: #3B4455;
      --fill-color: #D2E3FC;
      --hover-bg-color: #434B5C;
      --hover-fill-color: #FFFFFF;
      --disabled-bg-color: #3B4455;
      --disabled-fill-color: #666;
  }

  .colab-df-quickchart {
    background-color: var(--bg-color);
    border: none;
    border-radius: 50%;
    cursor: pointer;
    display: none;
    fill: var(--fill-color);
    height: 32px;
    padding: 0;
    width: 32px;
  }

  .colab-df-quickchart:hover {
    background-color: var(--hover-bg-color);
    box-shadow: 0 1px 2px rgba(60, 64, 67, 0.3), 0 1px 3px 1px rgba(60, 64, 67, 0.15);
    fill: var(--button-hover-fill-color);
  }

  .colab-df-quickchart-complete:disabled,
  .colab-df-quickchart-complete:disabled:hover {
    background-color: var(--disabled-bg-color);
    fill: var(--disabled-fill-color);
    box-shadow: none;
  }

  .colab-df-spinner {
    border: 2px solid var(--fill-color);
    border-color: transparent;
    border-bottom-color: var(--fill-color);
    animation:
      spin 1s steps(1) infinite;
  }

  @keyframes spin {
    0% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
      border-left-color: var(--fill-color);
    }
    20% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    30% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
      border-right-color: var(--fill-color);
    }
    40% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    60% {
      border-color: transparent;
      border-right-color: var(--fill-color);
    }
    80% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-bottom-color: var(--fill-color);
    }
    90% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
    }
  }
</style>

      <script>
        async function quickchart(key) {
          const quickchartButtonEl =
            document.querySelector('#' + key + ' button');
          quickchartButtonEl.disabled = true;  // To prevent multiple clicks.
          quickchartButtonEl.classList.add('colab-df-spinner');
          try {
            const charts = await google.colab.kernel.invokeFunction(
                'suggestCharts', [key], {});
          } catch (error) {
            console.error('Error during call to suggestCharts:', error);
          }
          quickchartButtonEl.classList.remove('colab-df-spinner');
          quickchartButtonEl.classList.add('colab-df-quickchart-complete');
        }
        (() => {
          let quickchartButtonEl =
            document.querySelector('#df-605dc61f-5b70-43ac-8d38-d4baab0d7d8d button');
          quickchartButtonEl.style.display =
            google.colab.kernel.accessAllowed ? 'block' : 'none';
        })();
      </script>
    </div>

    </div>
  </div>
</div>
</div>
<div id="cell-8" class="cell" data-executioninfo="{&quot;status&quot;:&quot;ok&quot;,&quot;timestamp&quot;:1745761247812,&quot;user_tz&quot;:-60,&quot;elapsed&quot;:849,&quot;user&quot;:{&quot;displayName&quot;:&quot;Omkar Mamidwar&quot;,&quot;userId&quot;:&quot;12811350756920516353&quot;}}" data-outputid="19c1931d-d8c3-4a6d-d568-8e13d093930d" data-execution_count="9">
<div class="sourceCode cell-code" id="cb10"><pre class="sourceCode python code-with-copy"><code class="sourceCode python"><span id="cb10-1"><a href="#cb10-1" aria-hidden="true" tabindex="-1"></a><span class="co"># Time series plot</span></span>
<span id="cb10-2"><a href="#cb10-2" aria-hidden="true" tabindex="-1"></a>mortality_ts <span class="op">=</span> combined.groupby(<span class="st">'time_period'</span>)[<span class="st">'obs_value_x'</span>].<span class="bu">sum</span>().reset_index()</span>
<span id="cb10-3"><a href="#cb10-3" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb10-4"><a href="#cb10-4" aria-hidden="true" tabindex="-1"></a>(pn.ggplot(mortality_ts, pn.aes(x<span class="op">=</span><span class="st">'time_period'</span>, y<span class="op">=</span><span class="st">'obs_value_x'</span>)) <span class="op">+</span></span>
<span id="cb10-5"><a href="#cb10-5" aria-hidden="true" tabindex="-1"></a> pn.geom_area(fill<span class="op">=</span><span class="st">'sienna'</span>, alpha<span class="op">=</span><span class="fl">0.7</span>) <span class="op">+</span></span>
<span id="cb10-6"><a href="#cb10-6" aria-hidden="true" tabindex="-1"></a> pn.geom_text(pn.aes(label<span class="op">=</span><span class="st">'obs_value_x'</span>), va<span class="op">=</span><span class="st">'bottom'</span>, size<span class="op">=</span><span class="dv">8</span>, nudge_y<span class="op">=</span><span class="dv">100</span>) <span class="op">+</span></span>
<span id="cb10-7"><a href="#cb10-7" aria-hidden="true" tabindex="-1"></a> pn.theme_minimal() <span class="op">+</span></span>
<span id="cb10-8"><a href="#cb10-8" aria-hidden="true" tabindex="-1"></a> pn.labs(title<span class="op">=</span><span class="st">"Maternal observation value by time period"</span>, x<span class="op">=</span><span class="st">"time_period"</span>, y<span class="op">=</span><span class="st">"obs_value_x"</span>)<span class="op">+</span></span>
<span id="cb10-9"><a href="#cb10-9" aria-hidden="true" tabindex="-1"></a>  pn.theme(figure_size<span class="op">=</span>(<span class="dv">16</span>, <span class="dv">6</span>)))</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-display">
<div>
<figure class="figure">
<p><img src="unicef1_files/figure-html/cell-10-output-1.png" width="1600" height="600" class="figure-img"></p>
</figure>
</div>
</div>
</div>
<div id="cell-9" class="cell" data-executioninfo="{&quot;status&quot;:&quot;ok&quot;,&quot;timestamp&quot;:1745761264203,&quot;user_tz&quot;:-60,&quot;elapsed&quot;:410,&quot;user&quot;:{&quot;displayName&quot;:&quot;Omkar Mamidwar&quot;,&quot;userId&quot;:&quot;12811350756920516353&quot;}}" data-outputid="a1415003-30c1-4b3f-ed08-f40deaddbcb6" data-execution_count="10">
<div class="sourceCode cell-code" id="cb11"><pre class="sourceCode python code-with-copy"><code class="sourceCode python"><span id="cb11-1"><a href="#cb11-1" aria-hidden="true" tabindex="-1"></a><span class="co"># Top countries by maternal mortality</span></span>
<span id="cb11-2"><a href="#cb11-2" aria-hidden="true" tabindex="-1"></a>top_countries <span class="op">=</span> combined.groupby(<span class="st">'country'</span>)[<span class="st">'obs_value_x'</span>].<span class="bu">sum</span>().nlargest(<span class="dv">6</span>).reset_index()</span>
<span id="cb11-3"><a href="#cb11-3" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb11-4"><a href="#cb11-4" aria-hidden="true" tabindex="-1"></a>(pn.ggplot(top_countries, pn.aes(x<span class="op">=</span><span class="st">'country'</span>, y<span class="op">=</span><span class="st">'obs_value_x'</span>, fill<span class="op">=</span><span class="st">'country'</span>)) <span class="op">+</span></span>
<span id="cb11-5"><a href="#cb11-5" aria-hidden="true" tabindex="-1"></a> pn.geom_col(show_legend<span class="op">=</span><span class="va">False</span>) <span class="op">+</span></span>
<span id="cb11-6"><a href="#cb11-6" aria-hidden="true" tabindex="-1"></a> pn.coord_flip() <span class="op">+</span></span>
<span id="cb11-7"><a href="#cb11-7" aria-hidden="true" tabindex="-1"></a> pn.theme_minimal() <span class="op">+</span></span>
<span id="cb11-8"><a href="#cb11-8" aria-hidden="true" tabindex="-1"></a> pn.labs(title<span class="op">=</span><span class="st">"Maternal Mortality Trends by Country and Time"</span>, x<span class="op">=</span><span class="st">"Country"</span>, y<span class="op">=</span><span class="st">"Observation Value"</span>)<span class="op">+</span></span>
<span id="cb11-9"><a href="#cb11-9" aria-hidden="true" tabindex="-1"></a> pn.theme(figure_size<span class="op">=</span>(<span class="dv">16</span>, <span class="dv">6</span>)))</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-display">
<div>
<figure class="figure">
<p><img src="unicef1_files/figure-html/cell-11-output-1.png" width="1600" height="600" class="figure-img"></p>
</figure>
</div>
</div>
</div>
<div id="cell-10" class="cell" data-executioninfo="{&quot;status&quot;:&quot;ok&quot;,&quot;timestamp&quot;:1745761280724,&quot;user_tz&quot;:-60,&quot;elapsed&quot;:2589,&quot;user&quot;:{&quot;displayName&quot;:&quot;Omkar Mamidwar&quot;,&quot;userId&quot;:&quot;12811350756920516353&quot;}}" data-outputid="9de442bb-c131-4f4f-af8b-4c2e575880b9" data-execution_count="11">
<div class="sourceCode cell-code" id="cb12"><pre class="sourceCode python code-with-copy"><code class="sourceCode python"><span id="cb12-1"><a href="#cb12-1" aria-hidden="true" tabindex="-1"></a><span class="co"># Gallery, points</span></span>
<span id="cb12-2"><a href="#cb12-2" aria-hidden="true" tabindex="-1"></a>(</span>
<span id="cb12-3"><a href="#cb12-3" aria-hidden="true" tabindex="-1"></a>    pn.ggplot(combined, pn.aes(<span class="st">"time_period"</span>, <span class="st">"Life expectancy at birth, total (years)"</span>, size<span class="op">=</span><span class="st">"obs_value_y"</span>)) <span class="co"># Replace var1 with an actual column from your dataframe - obs_value_y</span></span>
<span id="cb12-4"><a href="#cb12-4" aria-hidden="true" tabindex="-1"></a>    <span class="op">+</span> pn.geom_point(pn.aes(fill<span class="op">=</span><span class="st">"obs_value_x"</span>), stroke<span class="op">=</span><span class="dv">0</span>, alpha<span class="op">=</span><span class="fl">0.5</span>) <span class="co"># Replace var2 with an actual column - country</span></span>
<span id="cb12-5"><a href="#cb12-5" aria-hidden="true" tabindex="-1"></a>    <span class="op">+</span>pn.theme(figure_size<span class="op">=</span>(<span class="dv">16</span>, <span class="dv">6</span>)))<span class="co"># Replace var2 with an actual column - country</span></span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-stderr">
<pre><code>/usr/local/lib/python3.11/dist-packages/plotnine/layer.py:364: PlotnineWarning: geom_point : Removed 240221 rows containing missing values.</code></pre>
</div>
<div class="cell-output cell-output-display">
<div>
<figure class="figure">
<p><img src="unicef1_files/figure-html/cell-12-output-2.png" width="1600" height="600" class="figure-img"></p>
</figure>
</div>
</div>
</div>
<div id="cell-11" class="cell" data-executioninfo="{&quot;status&quot;:&quot;ok&quot;,&quot;timestamp&quot;:1745771086803,&quot;user_tz&quot;:-60,&quot;elapsed&quot;:96,&quot;user&quot;:{&quot;displayName&quot;:&quot;Omkar Mamidwar&quot;,&quot;userId&quot;:&quot;12811350756920516353&quot;}}" data-outputid="cd50c474-a6f7-494b-eda3-ed290bc85bc0" data-execution_count="14">
<div class="sourceCode cell-code" id="cb14"><pre class="sourceCode python code-with-copy"><code class="sourceCode python"><span id="cb14-1"><a href="#cb14-1" aria-hidden="true" tabindex="-1"></a><span class="im">import</span> pandas <span class="im">as</span> pd</span>
<span id="cb14-2"><a href="#cb14-2" aria-hidden="true" tabindex="-1"></a><span class="im">import</span> plotly.express <span class="im">as</span> px</span>
<span id="cb14-3"><a href="#cb14-3" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb14-4"><a href="#cb14-4" aria-hidden="true" tabindex="-1"></a><span class="co"># 1. Load the CSV file</span></span>
<span id="cb14-5"><a href="#cb14-5" aria-hidden="true" tabindex="-1"></a>df <span class="op">=</span> pd.read_csv(<span class="st">"/content/unicef_indicator_1.csv"</span>)</span>
<span id="cb14-6"><a href="#cb14-6" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb14-7"><a href="#cb14-7" aria-hidden="true" tabindex="-1"></a><span class="co"># 2. List of countries (your provided array)</span></span>
<span id="cb14-8"><a href="#cb14-8" aria-hidden="true" tabindex="-1"></a>countries <span class="op">=</span> [</span>
<span id="cb14-9"><a href="#cb14-9" aria-hidden="true" tabindex="-1"></a>    <span class="st">'Afghanistan'</span>, <span class="st">'Albania'</span>, <span class="st">'Algeria'</span>, <span class="st">'Angola'</span>, <span class="st">'Antigua and Barbuda'</span>,</span>
<span id="cb14-10"><a href="#cb14-10" aria-hidden="true" tabindex="-1"></a>    <span class="st">'Argentina'</span>, <span class="st">'Armenia'</span>, <span class="st">'Australia'</span>, <span class="st">'Austria'</span>, <span class="st">'Azerbaijan'</span>, <span class="st">'Bahamas'</span>,</span>
<span id="cb14-11"><a href="#cb14-11" aria-hidden="true" tabindex="-1"></a>    <span class="st">'Bahrain'</span>, <span class="st">'Bangladesh'</span>, <span class="st">'Barbados'</span>, <span class="st">'Belarus'</span>, <span class="st">'Belgium'</span>, <span class="st">'Belize'</span>,</span>
<span id="cb14-12"><a href="#cb14-12" aria-hidden="true" tabindex="-1"></a>    <span class="st">'Benin'</span>, <span class="st">'Bhutan'</span>, <span class="st">'Bolivia, Plurinational State of'</span>, <span class="st">'Bosnia and Herzegovina'</span>,</span>
<span id="cb14-13"><a href="#cb14-13" aria-hidden="true" tabindex="-1"></a>    <span class="st">'Botswana'</span>, <span class="st">'Brazil'</span>, <span class="st">'Brunei'</span>, <span class="st">'Bulgaria'</span>, <span class="st">'Burkina Faso'</span>, <span class="st">'Burundi'</span>,</span>
<span id="cb14-14"><a href="#cb14-14" aria-hidden="true" tabindex="-1"></a>    <span class="st">'Cambodia'</span>, <span class="st">'Cameroon'</span>, <span class="st">'Canada'</span>, <span class="st">'Cape Verde'</span>, <span class="st">'Central African Republic'</span>,</span>
<span id="cb14-15"><a href="#cb14-15" aria-hidden="true" tabindex="-1"></a>    <span class="st">'Chad'</span>, <span class="st">'Chile'</span>, <span class="st">'China'</span>, <span class="st">'Colombia'</span>, <span class="st">'Comoros'</span>, <span class="st">'Congo'</span>,</span>
<span id="cb14-16"><a href="#cb14-16" aria-hidden="true" tabindex="-1"></a>    <span class="st">'Congo, the Democratic Republic of the'</span>, <span class="st">'Costa Rica'</span>, <span class="st">'Croatia'</span>, <span class="st">'Cuba'</span>,</span>
<span id="cb14-17"><a href="#cb14-17" aria-hidden="true" tabindex="-1"></a>    <span class="st">'Cyprus'</span>, <span class="st">'Czech Republic'</span>, <span class="st">'Denmark'</span>, <span class="st">'Djibouti'</span>, <span class="st">'Dominican Republic'</span>,</span>
<span id="cb14-18"><a href="#cb14-18" aria-hidden="true" tabindex="-1"></a>    <span class="st">'Ecuador'</span>, <span class="st">'Egypt'</span>, <span class="st">'El Salvador'</span>, <span class="st">'Equatorial Guinea'</span>, <span class="st">'Eritrea'</span>,</span>
<span id="cb14-19"><a href="#cb14-19" aria-hidden="true" tabindex="-1"></a>    <span class="st">'Estonia'</span>, <span class="st">'Ethiopia'</span>, <span class="st">'Fiji'</span>, <span class="st">'Finland'</span>, <span class="st">'France'</span>, <span class="st">'Gabon'</span>, <span class="st">'Gambia'</span>,</span>
<span id="cb14-20"><a href="#cb14-20" aria-hidden="true" tabindex="-1"></a>    <span class="st">'Georgia'</span>, <span class="st">'Germany'</span>, <span class="st">'Ghana'</span>, <span class="st">'Greece'</span>, <span class="st">'Grenada'</span>, <span class="st">'Guatemala'</span>, <span class="st">'Guinea'</span>,</span>
<span id="cb14-21"><a href="#cb14-21" aria-hidden="true" tabindex="-1"></a>    <span class="st">'Guinea-Bissau'</span>, <span class="st">'Guyana'</span>, <span class="st">'Haiti'</span>, <span class="st">'Honduras'</span>, <span class="st">'Hungary'</span>, <span class="st">'Iceland'</span>,</span>
<span id="cb14-22"><a href="#cb14-22" aria-hidden="true" tabindex="-1"></a>    <span class="st">'India'</span>, <span class="st">'Indonesia'</span>, <span class="st">'Iran, Islamic Republic of'</span>, <span class="st">'Iraq'</span>, <span class="st">'Ireland'</span>,</span>
<span id="cb14-23"><a href="#cb14-23" aria-hidden="true" tabindex="-1"></a>    <span class="st">'Israel'</span>, <span class="st">'Italy'</span>, <span class="st">'Ivory Coast'</span>, <span class="st">'Jamaica'</span>, <span class="st">'Japan'</span>, <span class="st">'Jordan'</span>, <span class="st">'Kazakhstan'</span>,</span>
<span id="cb14-24"><a href="#cb14-24" aria-hidden="true" tabindex="-1"></a>    <span class="st">'Kenya'</span>, <span class="st">'Kiribati'</span>, <span class="st">"Korea, Democratic People's Republic of"</span>, <span class="st">'Kuwait'</span>,</span>
<span id="cb14-25"><a href="#cb14-25" aria-hidden="true" tabindex="-1"></a>    <span class="st">'Kyrgyzstan'</span>, <span class="st">"Lao People's Democratic Republic"</span>, <span class="st">'Latvia'</span>, <span class="st">'Lebanon'</span>,</span>
<span id="cb14-26"><a href="#cb14-26" aria-hidden="true" tabindex="-1"></a>    <span class="st">'Lesotho'</span>, <span class="st">'Liberia'</span>, <span class="st">'Libyan Arab Jamahiriya'</span>, <span class="st">'Lithuania'</span>, <span class="st">'Luxembourg'</span>,</span>
<span id="cb14-27"><a href="#cb14-27" aria-hidden="true" tabindex="-1"></a>    <span class="st">'Macedonia, the former Yugoslav Republic of'</span>, <span class="st">'Madagascar'</span>, <span class="st">'Malawi'</span>,</span>
<span id="cb14-28"><a href="#cb14-28" aria-hidden="true" tabindex="-1"></a>    <span class="st">'Malaysia'</span>, <span class="st">'Maldives'</span>, <span class="st">'Mali'</span>, <span class="st">'Malta'</span>, <span class="st">'Mauritania'</span>, <span class="st">'Mauritius'</span>,</span>
<span id="cb14-29"><a href="#cb14-29" aria-hidden="true" tabindex="-1"></a>    <span class="st">'Mexico'</span>, <span class="st">'Micronesia, Federated States of'</span>, <span class="st">'Moldova, Republic of'</span>,</span>
<span id="cb14-30"><a href="#cb14-30" aria-hidden="true" tabindex="-1"></a>    <span class="st">'Mongolia'</span>, <span class="st">'Montenegro'</span>, <span class="st">'Morocco'</span>, <span class="st">'Mozambique'</span>, <span class="st">'Myanmar'</span>, <span class="st">'Namibia'</span>,</span>
<span id="cb14-31"><a href="#cb14-31" aria-hidden="true" tabindex="-1"></a>    <span class="st">'Nauru'</span>, <span class="st">'Nepal'</span>, <span class="st">'Netherlands'</span>, <span class="st">'New Zealand'</span>, <span class="st">'Nicaragua'</span>, <span class="st">'Niger'</span>,</span>
<span id="cb14-32"><a href="#cb14-32" aria-hidden="true" tabindex="-1"></a>    <span class="st">'Nigeria'</span>, <span class="st">'Niue'</span>, <span class="st">'Norway'</span>, <span class="st">'Oman'</span>, <span class="st">'Pakistan'</span>, <span class="st">'Palestinian Territory, Occupied'</span>,</span>
<span id="cb14-33"><a href="#cb14-33" aria-hidden="true" tabindex="-1"></a>    <span class="st">'Panama'</span>, <span class="st">'Papua New Guinea'</span>, <span class="st">'Paraguay'</span>, <span class="st">'Peru'</span>, <span class="st">'Philippines'</span>, <span class="st">'Poland'</span>,</span>
<span id="cb14-34"><a href="#cb14-34" aria-hidden="true" tabindex="-1"></a>    <span class="st">'Portugal'</span>, <span class="st">'Puerto Rico'</span>, <span class="st">'Qatar'</span>, <span class="st">'Romania'</span>, <span class="st">'Russian Federation'</span>, <span class="st">'Rwanda'</span>,</span>
<span id="cb14-35"><a href="#cb14-35" aria-hidden="true" tabindex="-1"></a>    <span class="st">'Saint Lucia'</span>, <span class="st">'Samoa'</span>, <span class="st">'Sao Tome and Principe'</span>, <span class="st">'Saudi Arabia'</span>, <span class="st">'Senegal'</span>,</span>
<span id="cb14-36"><a href="#cb14-36" aria-hidden="true" tabindex="-1"></a>    <span class="st">'Serbia'</span>, <span class="st">'Seychelles'</span>, <span class="st">'Sierra Leone'</span>, <span class="st">'Singapore'</span>, <span class="st">'Slovakia'</span>, <span class="st">'Slovenia'</span>,</span>
<span id="cb14-37"><a href="#cb14-37" aria-hidden="true" tabindex="-1"></a>    <span class="st">'Solomon Islands'</span>, <span class="st">'Somalia'</span>, <span class="st">'South Africa'</span>, <span class="st">'South Korea'</span>, <span class="st">'South Sudan'</span>,</span>
<span id="cb14-38"><a href="#cb14-38" aria-hidden="true" tabindex="-1"></a>    <span class="st">'Spain'</span>, <span class="st">'Sri Lanka'</span>, <span class="st">'St. Vincent and the Grenadines'</span>, <span class="st">'Sudan'</span>, <span class="st">'Suriname'</span>,</span>
<span id="cb14-39"><a href="#cb14-39" aria-hidden="true" tabindex="-1"></a>    <span class="st">'Swaziland'</span>, <span class="st">'Sweden'</span>, <span class="st">'Switzerland'</span>, <span class="st">'Syrian Arab Republic'</span>, <span class="st">'Tajikistan'</span>,</span>
<span id="cb14-40"><a href="#cb14-40" aria-hidden="true" tabindex="-1"></a>    <span class="st">'Tanzania, United Republic of'</span>, <span class="st">'Thailand'</span>, <span class="st">'Timor-Leste'</span>, <span class="st">'Togo'</span>, <span class="st">'Tonga'</span>,</span>
<span id="cb14-41"><a href="#cb14-41" aria-hidden="true" tabindex="-1"></a>    <span class="st">'Trinidad and Tobago'</span>, <span class="st">'Tunisia'</span>, <span class="st">'Turkey'</span>, <span class="st">'Turkmenistan'</span>, <span class="st">'Turks and Caicos Islands'</span>,</span>
<span id="cb14-42"><a href="#cb14-42" aria-hidden="true" tabindex="-1"></a>    <span class="st">'Tuvalu'</span>, <span class="st">'Uganda'</span>, <span class="st">'Ukraine'</span>, <span class="st">'United Arab Emirates'</span>, <span class="st">'United Kingdom'</span>,</span>
<span id="cb14-43"><a href="#cb14-43" aria-hidden="true" tabindex="-1"></a>    <span class="st">'United States'</span>, <span class="st">'Uruguay'</span>, <span class="st">'Uzbekistan'</span>, <span class="st">'Vanuatu'</span>, <span class="st">'Venezuela, Bolivarian Republic of'</span>,</span>
<span id="cb14-44"><a href="#cb14-44" aria-hidden="true" tabindex="-1"></a>    <span class="st">'Vietnam'</span>, <span class="st">'Yemen'</span>, <span class="st">'Zambia'</span>, <span class="st">'Zimbabwe'</span></span>
<span id="cb14-45"><a href="#cb14-45" aria-hidden="true" tabindex="-1"></a>]</span>
<span id="cb14-46"><a href="#cb14-46" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb14-47"><a href="#cb14-47" aria-hidden="true" tabindex="-1"></a><span class="co"># 3. Filter the dataframe</span></span>
<span id="cb14-48"><a href="#cb14-48" aria-hidden="true" tabindex="-1"></a>filtered_df <span class="op">=</span> df[df[<span class="st">'country'</span>].isin(countries)]</span>
<span id="cb14-49"><a href="#cb14-49" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb14-50"><a href="#cb14-50" aria-hidden="true" tabindex="-1"></a><span class="co"># 4. Plot using Plotly Express</span></span>
<span id="cb14-51"><a href="#cb14-51" aria-hidden="true" tabindex="-1"></a>fig <span class="op">=</span> px.choropleth(</span>
<span id="cb14-52"><a href="#cb14-52" aria-hidden="true" tabindex="-1"></a>    filtered_df,</span>
<span id="cb14-53"><a href="#cb14-53" aria-hidden="true" tabindex="-1"></a>    locations<span class="op">=</span><span class="st">"country"</span>,</span>
<span id="cb14-54"><a href="#cb14-54" aria-hidden="true" tabindex="-1"></a>    locationmode<span class="op">=</span><span class="st">"country names"</span>,</span>
<span id="cb14-55"><a href="#cb14-55" aria-hidden="true" tabindex="-1"></a>    color<span class="op">=</span><span class="st">"obs_value"</span>,</span>
<span id="cb14-56"><a href="#cb14-56" aria-hidden="true" tabindex="-1"></a>    color_continuous_scale<span class="op">=</span><span class="st">"Viridis"</span>,</span>
<span id="cb14-57"><a href="#cb14-57" aria-hidden="true" tabindex="-1"></a>    title<span class="op">=</span><span class="st">"Global Visualization of Observation Values by Country"</span></span>
<span id="cb14-58"><a href="#cb14-58" aria-hidden="true" tabindex="-1"></a>)</span>
<span id="cb14-59"><a href="#cb14-59" aria-hidden="true" tabindex="-1"></a></span>
<span id="cb14-60"><a href="#cb14-60" aria-hidden="true" tabindex="-1"></a>fig.update_layout(geo<span class="op">=</span><span class="bu">dict</span>(showframe<span class="op">=</span><span class="va">False</span>, showcoastlines<span class="op">=</span><span class="va">False</span>))</span>
<span id="cb14-61"><a href="#cb14-61" aria-hidden="true" tabindex="-1"></a>fig.show()</span></code><button title="Copy to Clipboard" class="code-copy-button"><i class="bi"></i></button></pre></div>
<div class="cell-output cell-output-display">

<meta charset="utf-8">

    <div>            <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/MathJax.js?config=TeX-AMS-MML_SVG"></script><script type="text/javascript">if (window.MathJax && window.MathJax.Hub && window.MathJax.Hub.Config) {window.MathJax.Hub.Config({SVG: {font: "STIX-Web"}});}</script>                <script type="text/javascript">window.PlotlyConfig = {MathJaxConfig: 'local'};</script>
        <script charset="utf-8" src="https://cdn.plot.ly/plotly-2.35.2.min.js"></script>                <div id="902eff77-8c93-417a-8acb-44b69e167d64" class="plotly-graph-div" style="height:525px; width:100%;"></div>            <script type="text/javascript">                                    window.PLOTLYENV=window.PLOTLYENV || {};                                    if (document.getElementById("902eff77-8c93-417a-8acb-44b69e167d64")) {                    Plotly.newPlot(                        "902eff77-8c93-417a-8acb-44b69e167d64",                        [{"coloraxis":"coloraxis","geo":"geo","hovertemplate":"country=%{location}\u003cbr\u003eobs_value=%{z}\u003cextra\u003e\u003c\u002fextra\u003e","locationmode":"country names","locations":["Afghanistan","Afghanistan","Afghanistan","Afghanistan","Afghanistan","Afghanistan","Afghanistan","Afghanistan","Afghanistan","Afghanistan","Afghanistan","Afghanistan","Afghanistan","Afghanistan","Afghanistan","Afghanistan","Afghanistan","Afghanistan","Afghanistan","Afghanistan","Afghanistan","Albania","Albania","Albania","Albania","Albania","Albania","Albania","Albania","Albania","Albania","Albania","Albania","Albania","Albania","Albania","Albania","Albania","Albania","Albania","Albania","Albania","Algeria","Algeria","Algeria","Algeria","Algeria","Algeria","Algeria","Algeria","Algeria","Algeria","Algeria","Algeria","Algeria","Algeria","Algeria","Algeria","Algeria","Algeria","Algeria","Algeria","Algeria","Angola","Angola","Angola","Angola","Angola","Angola","Angola","Angola","Angola","Angola","Angola","Angola","Angola","Angola","Angola","Angola","Angola","Angola","Angola","Angola","Angola","Antigua and Barbuda","Antigua and Barbuda","Antigua and Barbuda","Antigua and Barbuda","Antigua and Barbuda","Antigua and Barbuda","Antigua and Barbuda","Antigua and Barbuda","Antigua and Barbuda","Antigua and Barbuda","Antigua and Barbuda","Antigua and Barbuda","Antigua and Barbuda","Antigua and Barbuda","Antigua and Barbuda","Antigua and Barbuda","Antigua and Barbuda","Antigua and Barbuda","Antigua and Barbuda","Antigua and Barbuda","Antigua and Barbuda","Argentina","Argentina","Argentina","Argentina","Argentina","Argentina","Argentina","Argentina","Argentina","Argentina","Argentina","Argentina","Argentina","Argentina","Argentina","Argentina","Argentina","Argentina","Argentina","Argentina","Argentina","Armenia","Armenia","Armenia","Armenia","Armenia","Armenia","Armenia","Armenia","Armenia","Armenia","Armenia","Armenia","Armenia","Armenia","Armenia","Armenia","Armenia","Armenia","Armenia","Armenia","Armenia","Australia","Australia","Australia","Australia","Australia","Australia","Australia","Australia","Australia","Australia","Australia","Australia","Australia","Australia","Australia","Australia","Australia","Australia","Australia","Australia","Australia","Austria","Austria","Austria","Austria","Austria","Austria","Austria","Austria","Austria","Austria","Austria","Austria","Austria","Austria","Austria","Austria","Austria","Austria","Austria","Austria","Austria","Azerbaijan","Azerbaijan","Azerbaijan","Azerbaijan","Azerbaijan","Azerbaijan","Azerbaijan","Azerbaijan","Azerbaijan","Azerbaijan","Azerbaijan","Azerbaijan","Azerbaijan","Azerbaijan","Azerbaijan","Azerbaijan","Azerbaijan","Azerbaijan","Azerbaijan","Azerbaijan","Azerbaijan","Bahamas","Bahamas","Bahamas","Bahamas","Bahamas","Bahamas","Bahamas","Bahamas","Bahamas","Bahamas","Bahamas","Bahamas","Bahamas","Bahamas","Bahamas","Bahamas","Bahamas","Bahamas","Bahamas","Bahamas","Bahamas","Bahrain","Bahrain","Bahrain","Bahrain","Bahrain","Bahrain","Bahrain","Bahrain","Bahrain","Bahrain","Bahrain","Bahrain","Bahrain","Bahrain","Bahrain","Bahrain","Bahrain","Bahrain","Bahrain","Bahrain","Bahrain","Bangladesh","Bangladesh","Bangladesh","Bangladesh","Bangladesh","Bangladesh","Bangladesh","Bangladesh","Bangladesh","Bangladesh","Bangladesh","Bangladesh","Bangladesh","Bangladesh","Bangladesh","Bangladesh","Bangladesh","Bangladesh","Bangladesh","Bangladesh","Bangladesh","Barbados","Barbados","Barbados","Barbados","Barbados","Barbados","Barbados","Barbados","Barbados","Barbados","Barbados","Barbados","Barbados","Barbados","Barbados","Barbados","Barbados","Barbados","Barbados","Barbados","Barbados","Belarus","Belarus","Belarus","Belarus","Belarus","Belarus","Belarus","Belarus","Belarus","Belarus","Belarus","Belarus","Belarus","Belarus","Belarus","Belarus","Belarus","Belarus","Belarus","Belarus","Belarus","Belgium","Belgium","Belgium","Belgium","Belgium","Belgium","Belgium","Belgium","Belgium","Belgium","Belgium","Belgium","Belgium","Belgium","Belgium","Belgium","Belgium","Belgium","Belgium","Belgium","Belgium","Belize","Belize","Belize","Belize","Belize","Belize","Belize","Belize","Belize","Belize","Belize","Belize","Belize","Belize","Belize","Belize","Belize","Belize","Belize","Belize","Belize","Benin","Benin","Benin","Benin","Benin","Benin","Benin","Benin","Benin","Benin","Benin","Benin","Benin","Benin","Benin","Benin","Benin","Benin","Benin","Benin","Benin","Bhutan","Bhutan","Bhutan","Bhutan","Bhutan","Bhutan","Bhutan","Bhutan","Bhutan","Bhutan","Bhutan","Bhutan","Bhutan","Bhutan","Bhutan","Bhutan","Bhutan","Bhutan","Bhutan","Bhutan","Bhutan","Bolivia, Plurinational State of","Bolivia, Plurinational State of","Bolivia, Plurinational State of","Bolivia, Plurinational State of","Bolivia, Plurinational State of","Bolivia, Plurinational State of","Bolivia, Plurinational State of","Bolivia, Plurinational State of","Bolivia, Plurinational State of","Bolivia, Plurinational State of","Bolivia, Plurinational State of","Bolivia, Plurinational State of","Bolivia, Plurinational State of","Bolivia, Plurinational State of","Bolivia, Plurinational State of","Bolivia, Plurinational State of","Bolivia, Plurinational State of","Bolivia, Plurinational State of","Bolivia, Plurinational State of","Bolivia, Plurinational State of","Bolivia, Plurinational State of","Bosnia and Herzegovina","Bosnia and Herzegovina","Bosnia and Herzegovina","Bosnia and Herzegovina","Bosnia and Herzegovina","Bosnia and Herzegovina","Bosnia and Herzegovina","Bosnia and Herzegovina","Bosnia and Herzegovina","Bosnia and Herzegovina","Bosnia and Herzegovina","Bosnia and Herzegovina","Bosnia and Herzegovina","Bosnia and Herzegovina","Bosnia and Herzegovina","Bosnia and Herzegovina","Bosnia and Herzegovina","Bosnia and Herzegovina","Bosnia and Herzegovina","Bosnia and Herzegovina","Bosnia and Herzegovina","Botswana","Botswana","Botswana","Botswana","Botswana","Botswana","Botswana","Botswana","Botswana","Botswana","Botswana","Botswana","Botswana","Botswana","Botswana","Botswana","Botswana","Botswana","Botswana","Botswana","Botswana","Brazil","Brazil","Brazil","Brazil","Brazil","Brazil","Brazil","Brazil","Brazil","Brazil","Brazil","Brazil","Brazil","Brazil","Brazil","Brazil","Brazil","Brazil","Brazil","Brazil","Brazil","Brunei","Brunei","Brunei","Brunei","Brunei","Brunei","Brunei","Brunei","Brunei","Brunei","Brunei","Brunei","Brunei","Brunei","Brunei","Brunei","Brunei","Brunei","Brunei","Brunei","Brunei","Bulgaria","Bulgaria","Bulgaria","Bulgaria","Bulgaria","Bulgaria","Bulgaria","Bulgaria","Bulgaria","Bulgaria","Bulgaria","Bulgaria","Bulgaria","Bulgaria","Bulgaria","Bulgaria","Bulgaria","Bulgaria","Bulgaria","Bulgaria","Bulgaria","Burkina Faso","Burkina Faso","Burkina Faso","Burkina Faso","Burkina Faso","Burkina Faso","Burkina Faso","Burkina Faso","Burkina Faso","Burkina Faso","Burkina Faso","Burkina Faso","Burkina Faso","Burkina Faso","Burkina Faso","Burkina Faso","Burkina Faso","Burkina Faso","Burkina Faso","Burkina Faso","Burkina Faso","Burundi","Burundi","Burundi","Burundi","Burundi","Burundi","Burundi","Burundi","Burundi","Burundi","Burundi","Burundi","Burundi","Burundi","Burundi","Burundi","Burundi","Burundi","Burundi","Burundi","Burundi","Cape Verde","Cape Verde","Cape Verde","Cape Verde","Cape Verde","Cape Verde","Cape Verde","Cape Verde","Cape Verde","Cape Verde","Cape Verde","Cape Verde","Cape Verde","Cape Verde","Cape Verde","Cape Verde","Cape Verde","Cape Verde","Cape Verde","Cape Verde","Cape Verde","Cambodia","Cambodia","Cambodia","Cambodia","Cambodia","Cambodia","Cambodia","Cambodia","Cambodia","Cambodia","Cambodia","Cambodia","Cambodia","Cambodia","Cambodia","Cambodia","Cambodia","Cambodia","Cambodia","Cambodia","Cambodia","Cameroon","Cameroon","Cameroon","Cameroon","Cameroon","Cameroon","Cameroon","Cameroon","Cameroon","Cameroon","Cameroon","Cameroon","Cameroon","Cameroon","Cameroon","Cameroon","Cameroon","Cameroon","Cameroon","Cameroon","Cameroon","Canada","Canada","Canada","Canada","Canada","Canada","Canada","Canada","Canada","Canada","Canada","Canada","Canada","Canada","Canada","Canada","Canada","Canada","Canada","Canada","Canada","Central African Republic","Central African Republic","Central African Republic","Central African Republic","Central African Republic","Central African Republic","Central African Republic","Central African Republic","Central African Republic","Central African Republic","Central African Republic","Central African Republic","Central African Republic","Central African Republic","Central African Republic","Central African Republic","Central African Republic","Central African Republic","Central African Republic","Central African Republic","Central African Republic","Chad","Chad","Chad","Chad","Chad","Chad","Chad","Chad","Chad","Chad","Chad","Chad","Chad","Chad","Chad","Chad","Chad","Chad","Chad","Chad","Chad","Chile","Chile","Chile","Chile","Chile","Chile","Chile","Chile","Chile","Chile","Chile","Chile","Chile","Chile","Chile","Chile","Chile","Chile","Chile","Chile","Chile","China","China","China","China","China","China","China","China","China","China","China","China","China","China","China","China","China","China","China","China","China","Colombia","Colombia","Colombia","Colombia","Colombia","Colombia","Colombia","Colombia","Colombia","Colombia","Colombia","Colombia","Colombia","Colombia","Colombia","Colombia","Colombia","Colombia","Colombia","Colombia","Colombia","Comoros","Comoros","Comoros","Comoros","Comoros","Comoros","Comoros","Comoros","Comoros","Comoros","Comoros","Comoros","Comoros","Comoros","Comoros","Comoros","Comoros","Comoros","Comoros","Comoros","Comoros","Congo","Congo","Congo","Congo","Congo","Congo","Congo","Congo","Congo","Congo","Congo","Congo","Congo","Congo","Congo","Congo","Congo","Congo","Congo","Congo","Congo","Costa Rica","Costa Rica","Costa Rica","Costa Rica","Costa Rica","Costa Rica","Costa Rica","Costa Rica","Costa Rica","Costa Rica","Costa Rica","Costa Rica","Costa Rica","Costa Rica","Costa Rica","Costa Rica","Costa Rica","Costa Rica","Costa Rica","Costa Rica","Costa Rica","Croatia","Croatia","Croatia","Croatia","Croatia","Croatia","Croatia","Croatia","Croatia","Croatia","Croatia","Croatia","Croatia","Croatia","Croatia","Croatia","Croatia","Croatia","Croatia","Croatia","Croatia","Cuba","Cuba","Cuba","Cuba","Cuba","Cuba","Cuba","Cuba","Cuba","Cuba","Cuba","Cuba","Cuba","Cuba","Cuba","Cuba","Cuba","Cuba","Cuba","Cuba","Cuba","Cyprus","Cyprus","Cyprus","Cyprus","Cyprus","Cyprus","Cyprus","Cyprus","Cyprus","Cyprus","Cyprus","Cyprus","Cyprus","Cyprus","Cyprus","Cyprus","Cyprus","Cyprus","Cyprus","Cyprus","Cyprus","Czech Republic","Czech Republic","Czech Republic","Czech Republic","Czech Republic","Czech Republic","Czech Republic","Czech Republic","Czech Republic","Czech Republic","Czech Republic","Czech Republic","Czech Republic","Czech Republic","Czech Republic","Czech Republic","Czech Republic","Czech Republic","Czech Republic","Czech Republic","Czech Republic","Ivory Coast","Ivory Coast","Ivory Coast","Ivory Coast","Ivory Coast","Ivory Coast","Ivory Coast","Ivory Coast","Ivory Coast","Ivory Coast","Ivory Coast","Ivory Coast","Ivory Coast","Ivory Coast","Ivory Coast","Ivory Coast","Ivory Coast","Ivory Coast","Ivory Coast","Ivory Coast","Ivory Coast","Korea, Democratic People's Republic of","Korea, Democratic People's Republic of","Korea, Democratic People's Republic of","Korea, Democratic People's Republic of","Korea, Democratic People's Republic of","Korea, Democratic People's Republic of","Korea, Democratic People's Republic of","Korea, Democratic People's Republic of","Korea, Democratic People's Republic of","Korea, Democratic People's Republic of","Korea, Democratic People's Republic of","Korea, Democratic People's Republic of","Korea, Democratic People's Republic of","Korea, Democratic People's Republic of","Korea, Democratic People's Republic of","Korea, Democratic People's Republic of","Korea, Democratic People's Republic of","Korea, Democratic People's Republic of","Korea, Democratic People's Republic of","Korea, Democratic People's Republic of","Korea, Democratic People's Republic of","Congo, the Democratic Republic of the","Congo, the Democratic Republic of the","Congo, the Democratic Republic of the","Congo, the Democratic Republic of the","Congo, the Democratic Republic of the","Congo, the Democratic Republic of the","Congo, the Democratic Republic of the","Congo, the Democratic Republic of the","Congo, the Democratic Republic of the","Congo, the Democratic Republic of the","Congo, the Democratic Republic of the","Congo, the Democratic Republic of the","Congo, the Democratic Republic of the","Congo, the Democratic Republic of the","Congo, the Democratic Republic of the","Congo, the Democratic Republic of the","Congo, the Democratic Republic of the","Congo, the Democratic Republic of the","Congo, the Democratic Republic of the","Congo, the Democratic Republic of the","Congo, the Democratic Republic of the","Denmark","Denmark","Denmark","Denmark","Denmark","Denmark","Denmark","Denmark","Denmark","Denmark","Denmark","Denmark","Denmark","Denmark","Denmark","Denmark","Denmark","Denmark","Denmark","Denmark","Denmark","Djibouti","Djibouti","Djibouti","Djibouti","Djibouti","Djibouti","Djibouti","Djibouti","Djibouti","Djibouti","Djibouti","Djibouti","Djibouti","Djibouti","Djibouti","Djibouti","Djibouti","Djibouti","Djibouti","Djibouti","Djibouti","Dominican Republic","Dominican Republic","Dominican Republic","Dominican Republic","Dominican Republic","Dominican Republic","Dominican Republic","Dominican Republic","Dominican Republic","Dominican Republic","Dominican Republic","Dominican Republic","Dominican Republic","Dominican Republic","Dominican Republic","Dominican Republic","Dominican Republic","Dominican Republic","Dominican Republic","Dominican Republic","Dominican Republic","Ecuador","Ecuador","Ecuador","Ecuador","Ecuador","Ecuador","Ecuador","Ecuador","Ecuador","Ecuador","Ecuador","Ecuador","Ecuador","Ecuador","Ecuador","Ecuador","Ecuador","Ecuador","Ecuador","Ecuador","Ecuador","Egypt","Egypt","Egypt","Egypt","Egypt","Egypt","Egypt","Egypt","Egypt","Egypt","Egypt","Egypt","Egypt","Egypt","Egypt","Egypt","Egypt","Egypt","Egypt","Egypt","Egypt","El Salvador","El Salvador","El Salvador","El Salvador","El Salvador","El Salvador","El Salvador","El Salvador","El Salvador","El Salvador","El Salvador","El Salvador","El Salvador","El Salvador","El Salvador","El Salvador","El Salvador","El Salvador","El Salvador","El Salvador","El Salvador","Equatorial Guinea","Equatorial Guinea","Equatorial Guinea","Equatorial Guinea","Equatorial Guinea","Equatorial Guinea","Equatorial Guinea","Equatorial Guinea","Equatorial Guinea","Equatorial Guinea","Equatorial Guinea","Equatorial Guinea","Equatorial Guinea","Equatorial Guinea","Equatorial Guinea","Equatorial Guinea","Equatorial Guinea","Equatorial Guinea","Equatorial Guinea","Equatorial Guinea","Equatorial Guinea","Eritrea","Eritrea","Eritrea","Eritrea","Eritrea","Eritrea","Eritrea","Eritrea","Eritrea","Eritrea","Eritrea","Eritrea","Eritrea","Eritrea","Eritrea","Eritrea","Eritrea","Eritrea","Eritrea","Eritrea","Eritrea","Estonia","Estonia","Estonia","Estonia","Estonia","Estonia","Estonia","Estonia","Estonia","Estonia","Estonia","Estonia","Estonia","Estonia","Estonia","Estonia","Estonia","Estonia","Estonia","Estonia","Estonia","Swaziland","Swaziland","Swaziland","Swaziland","Swaziland","Swaziland","Swaziland","Swaziland","Swaziland","Swaziland","Swaziland","Swaziland","Swaziland","Swaziland","Swaziland","Swaziland","Swaziland","Swaziland","Swaziland","Swaziland","Swaziland","Ethiopia","Ethiopia","Ethiopia","Ethiopia","Ethiopia","Ethiopia","Ethiopia","Ethiopia","Ethiopia","Ethiopia","Ethiopia","Ethiopia","Ethiopia","Ethiopia","Ethiopia","Ethiopia","Ethiopia","Ethiopia","Ethiopia","Ethiopia","Ethiopia","Fiji","Fiji","Fiji","Fiji","Fiji","Fiji","Fiji","Fiji","Fiji","Fiji","Fiji","Fiji","Fiji","Fiji","Fiji","Fiji","Fiji","Fiji","Fiji","Fiji","Fiji","Finland","Finland","Finland","Finland","Finland","Finland","Finland","Finland","Finland","Finland","Finland","Finland","Finland","Finland","Finland","Finland","Finland","Finland","Finland","Finland","Finland","France","France","France","France","France","France","France","France","France","France","France","France","France","France","France","France","France","France","France","France","France","Gabon","Gabon","Gabon","Gabon","Gabon","Gabon","Gabon","Gabon","Gabon","Gabon","Gabon","Gabon","Gabon","Gabon","Gabon","Gabon","Gabon","Gabon","Gabon","Gabon","Gabon","Gambia","Gambia","Gambia","Gambia","Gambia","Gambia","Gambia","Gambia","Gambia","Gambia","Gambia","Gambia","Gambia","Gambia","Gambia","Gambia","Gambia","Gambia","Gambia","Gambia","Gambia","Georgia","Georgia","Georgia","Georgia","Georgia","Georgia","Georgia","Georgia","Georgia","Georgia","Georgia","Georgia","Georgia","Georgia","Georgia","Georgia","Georgia","Georgia","Georgia","Georgia","Georgia","Germany","Germany","Germany","Germany","Germany","Germany","Germany","Germany","Germany","Germany","Germany","Germany","Germany","Germany","Germany","Germany","Germany","Germany","Germany","Germany","Germany","Ghana","Ghana","Ghana","Ghana","Ghana","Ghana","Ghana","Ghana","Ghana","Ghana","Ghana","Ghana","Ghana","Ghana","Ghana","Ghana","Ghana","Ghana","Ghana","Ghana","Ghana","Greece","Greece","Greece","Greece","Greece","Greece","Greece","Greece","Greece","Greece","Greece","Greece","Greece","Greece","Greece","Greece","Greece","Greece","Greece","Greece","Greece","Grenada","Grenada","Grenada","Grenada","Grenada","Grenada","Grenada","Grenada","Grenada","Grenada","Grenada","Grenada","Grenada","Grenada","Grenada","Grenada","Grenada","Grenada","Grenada","Grenada","Grenada","Guatemala","Guatemala","Guatemala","Guatemala","Guatemala","Guatemala","Guatemala","Guatemala","Guatemala","Guatemala","Guatemala","Guatemala","Guatemala","Guatemala","Guatemala","Guatemala","Guatemala","Guatemala","Guatemala","Guatemala","Guatemala","Guinea","Guinea","Guinea","Guinea","Guinea","Guinea","Guinea","Guinea","Guinea","Guinea","Guinea","Guinea","Guinea","Guinea","Guinea","Guinea","Guinea","Guinea","Guinea","Guinea","Guinea","Guinea-Bissau","Guinea-Bissau","Guinea-Bissau","Guinea-Bissau","Guinea-Bissau","Guinea-Bissau","Guinea-Bissau","Guinea-Bissau","Guinea-Bissau","Guinea-Bissau","Guinea-Bissau","Guinea-Bissau","Guinea-Bissau","Guinea-Bissau","Guinea-Bissau","Guinea-Bissau","Guinea-Bissau","Guinea-Bissau","Guinea-Bissau","Guinea-Bissau","Guinea-Bissau","Guyana","Guyana","Guyana","Guyana","Guyana","Guyana","Guyana","Guyana","Guyana","Guyana","Guyana","Guyana","Guyana","Guyana","Guyana","Guyana","Guyana","Guyana","Guyana","Guyana","Guyana","Haiti","Haiti","Haiti","Haiti","Haiti","Haiti","Haiti","Haiti","Haiti","Haiti","Haiti","Haiti","Haiti","Haiti","Haiti","Haiti","Haiti","Haiti","Haiti","Haiti","Haiti","Honduras","Honduras","Honduras","Honduras","Honduras","Honduras","Honduras","Honduras","Honduras","Honduras","Honduras","Honduras","Honduras","Honduras","Honduras","Honduras","Honduras","Honduras","Honduras","Honduras","Honduras","Hungary","Hungary","Hungary","Hungary","Hungary","Hungary","Hungary","Hungary","Hungary","Hungary","Hungary","Hungary","Hungary","Hungary","Hungary","Hungary","Hungary","Hungary","Hungary","Hungary","Hungary","Iceland","Iceland","Iceland","Iceland","Iceland","Iceland","Iceland","Iceland","Iceland","Iceland","Iceland","Iceland","Iceland","Iceland","Iceland","Iceland","Iceland","Iceland","Iceland","Iceland","Iceland","India","India","India","India","India","India","India","India","India","India","India","India","India","India","India","India","India","India","India","India","India","Indonesia","Indonesia","Indonesia","Indonesia","Indonesia","Indonesia","Indonesia","Indonesia","Indonesia","Indonesia","Indonesia","Indonesia","Indonesia","Indonesia","Indonesia","Indonesia","Indonesia","Indonesia","Indonesia","Indonesia","Indonesia","Iran, Islamic Republic of","Iran, Islamic Republic of","Iran, Islamic Republic of","Iran, Islamic Republic of","Iran, Islamic Republic of","Iran, Islamic Republic of","Iran, Islamic Republic of","Iran, Islamic Republic of","Iran, Islamic Republic of","Iran, Islamic Republic of","Iran, Islamic Republic of","Iran, Islamic Republic of","Iran, Islamic Republic of","Iran, Islamic Republic of","Iran, Islamic Republic of","Iran, Islamic Republic of","Iran, Islamic Republic of","Iran, Islamic Republic of","Iran, Islamic Republic of","Iran, Islamic Republic of","Iran, Islamic Republic of","Iraq","Iraq","Iraq","Iraq","Iraq","Iraq","Iraq","Iraq","Iraq","Iraq","Iraq","Iraq","Iraq","Iraq","Iraq","Iraq","Iraq","Iraq","Iraq","Iraq","Iraq","Ireland","Ireland","Ireland","Ireland","Ireland","Ireland","Ireland","Ireland","Ireland","Ireland","Ireland","Ireland","Ireland","Ireland","Ireland","Ireland","Ireland","Ireland","Ireland","Ireland","Ireland","Israel","Israel","Israel","Israel","Israel","Israel","Israel","Israel","Israel","Israel","Israel","Israel","Israel","Israel","Israel","Israel","Israel","Israel","Israel","Israel","Israel","Italy","Italy","Italy","Italy","Italy","Italy","Italy","Italy","Italy","Italy","Italy","Italy","Italy","Italy","Italy","Italy","Italy","Italy","Italy","Italy","Italy","Jamaica","Jamaica","Jamaica","Jamaica","Jamaica","Jamaica","Jamaica","Jamaica","Jamaica","Jamaica","Jamaica","Jamaica","Jamaica","Jamaica","Jamaica","Jamaica","Jamaica","Jamaica","Jamaica","Jamaica","Jamaica","Japan","Japan","Japan","Japan","Japan","Japan","Japan","Japan","Japan","Japan","Japan","Japan","Japan","Japan","Japan","Japan","Japan","Japan","Japan","Japan","Japan","Jordan","Jordan","Jordan","Jordan","Jordan","Jordan","Jordan","Jordan","Jordan","Jordan","Jordan","Jordan","Jordan","Jordan","Jordan","Jordan","Jordan","Jordan","Jordan","Jordan","Jordan","Kazakhstan","Kazakhstan","Kazakhstan","Kazakhstan","Kazakhstan","Kazakhstan","Kazakhstan","Kazakhstan","Kazakhstan","Kazakhstan","Kazakhstan","Kazakhstan","Kazakhstan","Kazakhstan","Kazakhstan","Kazakhstan","Kazakhstan","Kazakhstan","Kazakhstan","Kazakhstan","Kazakhstan","Kenya","Kenya","Kenya","Kenya","Kenya","Kenya","Kenya","Kenya","Kenya","Kenya","Kenya","Kenya","Kenya","Kenya","Kenya","Kenya","Kenya","Kenya","Kenya","Kenya","Kenya","Kiribati","Kiribati","Kiribati","Kiribati","Kiribati","Kiribati","Kiribati","Kiribati","Kiribati","Kiribati","Kiribati","Kiribati","Kiribati","Kiribati","Kiribati","Kiribati","Kiribati","Kiribati","Kiribati","Kiribati","Kiribati","Kuwait","Kuwait","Kuwait","Kuwait","Kuwait","Kuwait","Kuwait","Kuwait","Kuwait","Kuwait","Kuwait","Kuwait","Kuwait","Kuwait","Kuwait","Kuwait","Kuwait","Kuwait","Kuwait","Kuwait","Kuwait","Kyrgyzstan","Kyrgyzstan","Kyrgyzstan","Kyrgyzstan","Kyrgyzstan","Kyrgyzstan","Kyrgyzstan","Kyrgyzstan","Kyrgyzstan","Kyrgyzstan","Kyrgyzstan","Kyrgyzstan","Kyrgyzstan","Kyrgyzstan","Kyrgyzstan","Kyrgyzstan","Kyrgyzstan","Kyrgyzstan","Kyrgyzstan","Kyrgyzstan","Kyrgyzstan","Lao People's Democratic Republic","Lao People's Democratic Republic","Lao People's Democratic Republic","Lao People's Democratic Republic","Lao People's Democratic Republic","Lao People's Democratic Republic","Lao People's Democratic Republic","Lao People's Democratic Republic","Lao People's Democratic Republic","Lao People's Democratic Republic","Lao People's Democratic Republic","Lao People's Democratic Republic","Lao People's Democratic Republic","Lao People's Democratic Republic","Lao People's Democratic Republic","Lao People's Democratic Republic","Lao People's Democratic Republic","Lao People's Democratic Republic","Lao People's Democratic Republic","Lao People's Democratic Republic","Lao People's Democratic Republic","Latvia","Latvia","Latvia","Latvia","Latvia","Latvia","Latvia","Latvia","Latvia","Latvia","Latvia","Latvia","Latvia","Latvia","Latvia","Latvia","Latvia","Latvia","Latvia","Latvia","Latvia","Lebanon","Lebanon","Lebanon","Lebanon","Lebanon","Lebanon","Lebanon","Lebanon","Lebanon","Lebanon","Lebanon","Lebanon","Lebanon","Lebanon","Lebanon","Lebanon","Lebanon","Lebanon","Lebanon","Lebanon","Lebanon","Lesotho","Lesotho","Lesotho","Lesotho","Lesotho","Lesotho","Lesotho","Lesotho","Lesotho","Lesotho","Lesotho","Lesotho","Lesotho","Lesotho","Lesotho","Lesotho","Lesotho","Lesotho","Lesotho","Lesotho","Lesotho","Liberia","Liberia","Liberia","Liberia","Liberia","Liberia","Liberia","Liberia","Liberia","Liberia","Liberia","Liberia","Liberia","Liberia","Liberia","Liberia","Liberia","Liberia","Liberia","Liberia","Liberia","Libyan Arab Jamahiriya","Libyan Arab Jamahiriya","Libyan Arab Jamahiriya","Libyan Arab Jamahiriya","Libyan Arab Jamahiriya","Libyan Arab Jamahiriya","Libyan Arab Jamahiriya","Libyan Arab Jamahiriya","Libyan Arab Jamahiriya","Libyan Arab Jamahiriya","Libyan Arab Jamahiriya","Libyan Arab Jamahiriya","Libyan Arab Jamahiriya","Libyan Arab Jamahiriya","Libyan Arab Jamahiriya","Libyan Arab Jamahiriya","Libyan Arab Jamahiriya","Libyan Arab Jamahiriya","Libyan Arab Jamahiriya","Libyan Arab Jamahiriya","Libyan Arab Jamahiriya","Lithuania","Lithuania","Lithuania","Lithuania","Lithuania","Lithuania","Lithuania","Lithuania","Lithuania","Lithuania","Lithuania","Lithuania","Lithuania","Lithuania","Lithuania","Lithuania","Lithuania","Lithuania","Lithuania","Lithuania","Lithuania","Luxembourg","Luxembourg","Luxembourg","Luxembourg","Luxembourg","Luxembourg","Luxembourg","Luxembourg","Luxembourg","Luxembourg","Luxembourg","Luxembourg","Luxembourg","Luxembourg","Luxembourg","Luxembourg","Luxembourg","Luxembourg","Luxembourg","Luxembourg","Luxembourg","Madagascar","Madagascar","Madagascar","Madagascar","Madagascar","Madagascar","Madagascar","Madagascar","Madagascar","Madagascar","Madagascar","Madagascar","Madagascar","Madagascar","Madagascar","Madagascar","Madagascar","Madagascar","Madagascar","Madagascar","Madagascar","Malawi","Malawi","Malawi","Malawi","Malawi","Malawi","Malawi","Malawi","Malawi","Malawi","Malawi","Malawi","Malawi","Malawi","Malawi","Malawi","Malawi","Malawi","Malawi","Malawi","Malawi","Malaysia","Malaysia","Malaysia","Malaysia","Malaysia","Malaysia","Malaysia","Malaysia","Malaysia","Malaysia","Malaysia","Malaysia","Malaysia","Malaysia","Malaysia","Malaysia","Malaysia","Malaysia","Malaysia","Malaysia","Malaysia","Maldives","Maldives","Maldives","Maldives","Maldives","Maldives","Maldives","Maldives","Maldives","Maldives","Maldives","Maldives","Maldives","Maldives","Maldives","Maldives","Maldives","Maldives","Maldives","Maldives","Maldives","Mali","Mali","Mali","Mali","Mali","Mali","Mali","Mali","Mali","Mali","Mali","Mali","Mali","Mali","Mali","Mali","Mali","Mali","Mali","Mali","Mali","Malta","Malta","Malta","Malta","Malta","Malta","Malta","Malta","Malta","Malta","Malta","Malta","Malta","Malta","Malta","Malta","Malta","Malta","Malta","Malta","Malta","Mauritania","Mauritania","Mauritania","Mauritania","Mauritania","Mauritania","Mauritania","Mauritania","Mauritania","Mauritania","Mauritania","Mauritania","Mauritania","Mauritania","Mauritania","Mauritania","Mauritania","Mauritania","Mauritania","Mauritania","Mauritania","Mauritius","Mauritius","Mauritius","Mauritius","Mauritius","Mauritius","Mauritius","Mauritius","Mauritius","Mauritius","Mauritius","Mauritius","Mauritius","Mauritius","Mauritius","Mauritius","Mauritius","Mauritius","Mauritius","Mauritius","Mauritius","Mexico","Mexico","Mexico","Mexico","Mexico","Mexico","Mexico","Mexico","Mexico","Mexico","Mexico","Mexico","Mexico","Mexico","Mexico","Mexico","Mexico","Mexico","Mexico","Mexico","Mexico","Micronesia, Federated States of","Micronesia, Federated States of","Micronesia, Federated States of","Micronesia, Federated States of","Micronesia, Federated States of","Micronesia, Federated States of","Micronesia, Federated States of","Micronesia, Federated States of","Micronesia, Federated States of","Micronesia, Federated States of","Micronesia, Federated States of","Micronesia, Federated States of","Micronesia, Federated States of","Micronesia, Federated States of","Micronesia, Federated States of","Micronesia, Federated States of","Micronesia, Federated States of","Micronesia, Federated States of","Micronesia, Federated States of","Micronesia, Federated States of","Micronesia, Federated States of","Mongolia","Mongolia","Mongolia","Mongolia","Mongolia","Mongolia","Mongolia","Mongolia","Mongolia","Mongolia","Mongolia","Mongolia","Mongolia","Mongolia","Mongolia","Mongolia","Mongolia","Mongolia","Mongolia","Mongolia","Mongolia","Montenegro","Montenegro","Montenegro","Montenegro","Montenegro","Montenegro","Montenegro","Montenegro","Montenegro","Montenegro","Montenegro","Montenegro","Montenegro","Montenegro","Montenegro","Montenegro","Montenegro","Montenegro","Montenegro","Montenegro","Montenegro","Morocco","Morocco","Morocco","Morocco","Morocco","Morocco","Morocco","Morocco","Morocco","Morocco","Morocco","Morocco","Morocco","Morocco","Morocco","Morocco","Morocco","Morocco","Morocco","Morocco","Morocco","Mozambique","Mozambique","Mozambique","Mozambique","Mozambique","Mozambique","Mozambique","Mozambique","Mozambique","Mozambique","Mozambique","Mozambique","Mozambique","Mozambique","Mozambique","Mozambique","Mozambique","Mozambique","Mozambique","Mozambique","Mozambique","Myanmar","Myanmar","Myanmar","Myanmar","Myanmar","Myanmar","Myanmar","Myanmar","Myanmar","Myanmar","Myanmar","Myanmar","Myanmar","Myanmar","Myanmar","Myanmar","Myanmar","Myanmar","Myanmar","Myanmar","Myanmar","Namibia","Namibia","Namibia","Namibia","Namibia","Namibia","Namibia","Namibia","Namibia","Namibia","Namibia","Namibia","Namibia","Namibia","Namibia","Namibia","Namibia","Namibia","Namibia","Namibia","Namibia","Nepal","Nepal","Nepal","Nepal","Nepal","Nepal","Nepal","Nepal","Nepal","Nepal","Nepal","Nepal","Nepal","Nepal","Nepal","Nepal","Nepal","Nepal","Nepal","Nepal","Nepal","Netherlands","Netherlands","Netherlands","Netherlands","Netherlands","Netherlands","Netherlands","Netherlands","Netherlands","Netherlands","Netherlands","Netherlands","Netherlands","Netherlands","Netherlands","Netherlands","Netherlands","Netherlands","Netherlands","Netherlands","Netherlands","New Zealand","New Zealand","New Zealand","New Zealand","New Zealand","New Zealand","New Zealand","New Zealand","New Zealand","New Zealand","New Zealand","New Zealand","New Zealand","New Zealand","New Zealand","New Zealand","New Zealand","New Zealand","New Zealand","New Zealand","New Zealand","Nicaragua","Nicaragua","Nicaragua","Nicaragua","Nicaragua","Nicaragua","Nicaragua","Nicaragua","Nicaragua","Nicaragua","Nicaragua","Nicaragua","Nicaragua","Nicaragua","Nicaragua","Nicaragua","Nicaragua","Nicaragua","Nicaragua","Nicaragua","Nicaragua","Niger","Niger","Niger","Niger","Niger","Niger","Niger","Niger","Niger","Niger","Niger","Niger","Niger","Niger","Niger","Niger","Niger","Niger","Niger","Niger","Niger","Nigeria","Nigeria","Nigeria","Nigeria","Nigeria","Nigeria","Nigeria","Nigeria","Nigeria","Nigeria","Nigeria","Nigeria","Nigeria","Nigeria","Nigeria","Nigeria","Nigeria","Nigeria","Nigeria","Nigeria","Nigeria","Macedonia, the former Yugoslav Republic of","Macedonia, the former Yugoslav Republic of","Macedonia, the former Yugoslav Republic of","Macedonia, the former Yugoslav Republic of","Macedonia, the former Yugoslav Republic of","Macedonia, the former Yugoslav Republic of","Macedonia, the former Yugoslav Republic of","Macedonia, the former Yugoslav Republic of","Macedonia, the former Yugoslav Republic of","Macedonia, the former Yugoslav Republic of","Macedonia, the former Yugoslav Republic of","Macedonia, the former Yugoslav Republic of","Macedonia, the former Yugoslav Republic of","Macedonia, the former Yugoslav Republic of","Macedonia, the former Yugoslav Republic of","Macedonia, the former Yugoslav Republic of","Macedonia, the former Yugoslav Republic of","Macedonia, the former Yugoslav Republic of","Macedonia, the former Yugoslav Republic of","Macedonia, the former Yugoslav Republic of","Macedonia, the former Yugoslav Republic of","Norway","Norway","Norway","Norway","Norway","Norway","Norway","Norway","Norway","Norway","Norway","Norway","Norway","Norway","Norway","Norway","Norway","Norway","Norway","Norway","Norway","Oman","Oman","Oman","Oman","Oman","Oman","Oman","Oman","Oman","Oman","Oman","Oman","Oman","Oman","Oman","Oman","Oman","Oman","Oman","Oman","Oman","Pakistan","Pakistan","Pakistan","Pakistan","Pakistan","Pakistan","Pakistan","Pakistan","Pakistan","Pakistan","Pakistan","Pakistan","Pakistan","Pakistan","Pakistan","Pakistan","Pakistan","Pakistan","Pakistan","Pakistan","Pakistan","Panama","Panama","Panama","Panama","Panama","Panama","Panama","Panama","Panama","Panama","Panama","Panama","Panama","Panama","Panama","Panama","Panama","Panama","Panama","Panama","Panama","Papua New Guinea","Papua New Guinea","Papua New Guinea","Papua New Guinea","Papua New Guinea","Papua New Guinea","Papua New Guinea","Papua New Guinea","Papua New Guinea","Papua New Guinea","Papua New Guinea","Papua New Guinea","Papua New Guinea","Papua New Guinea","Papua New Guinea","Papua New Guinea","Papua New Guinea","Papua New Guinea","Papua New Guinea","Papua New Guinea","Papua New Guinea","Paraguay","Paraguay","Paraguay","Paraguay","Paraguay","Paraguay","Paraguay","Paraguay","Paraguay","Paraguay","Paraguay","Paraguay","Paraguay","Paraguay","Paraguay","Paraguay","Paraguay","Paraguay","Paraguay","Paraguay","Paraguay","Peru","Peru","Peru","Peru","Peru","Peru","Peru","Peru","Peru","Peru","Peru","Peru","Peru","Peru","Peru","Peru","Peru","Peru","Peru","Peru","Peru","Philippines","Philippines","Philippines","Philippines","Philippines","Philippines","Philippines","Philippines","Philippines","Philippines","Philippines","Philippines","Philippines","Philippines","Philippines","Philippines","Philippines","Philippines","Philippines","Philippines","Philippines","Poland","Poland","Poland","Poland","Poland","Poland","Poland","Poland","Poland","Poland","Poland","Poland","Poland","Poland","Poland","Poland","Poland","Poland","Poland","Poland","Poland","Portugal","Portugal","Portugal","Portugal","Portugal","Portugal","Portugal","Portugal","Portugal","Portugal","Portugal","Portugal","Portugal","Portugal","Portugal","Portugal","Portugal","Portugal","Portugal","Portugal","Portugal","Puerto Rico","Puerto Rico","Puerto Rico","Puerto Rico","Puerto Rico","Puerto Rico","Puerto Rico","Puerto Rico","Puerto Rico","Puerto Rico","Puerto Rico","Puerto Rico","Puerto Rico","Puerto Rico","Puerto Rico","Puerto Rico","Puerto Rico","Puerto Rico","Puerto Rico","Puerto Rico","Puerto Rico","Qatar","Qatar","Qatar","Qatar","Qatar","Qatar","Qatar","Qatar","Qatar","Qatar","Qatar","Qatar","Qatar","Qatar","Qatar","Qatar","Qatar","Qatar","Qatar","Qatar","Qatar","South Korea","South Korea","South Korea","South Korea","South Korea","South Korea","South Korea","South Korea","South Korea","South Korea","South Korea","South Korea","South Korea","South Korea","South Korea","South Korea","South Korea","South Korea","South Korea","South Korea","South Korea","Moldova, Republic of","Moldova, Republic of","Moldova, Republic of","Moldova, Republic of","Moldova, Republic of","Moldova, Republic of","Moldova, Republic of","Moldova, Republic of","Moldova, Republic of","Moldova, Republic of","Moldova, Republic of","Moldova, Republic of","Moldova, Republic of","Moldova, Republic of","Moldova, Republic of","Moldova, Republic of","Moldova, Republic of","Moldova, Republic of","Moldova, Republic of","Moldova, Republic of","Moldova, Republic of","Romania","Romania","Romania","Romania","Romania","Romania","Romania","Romania","Romania","Romania","Romania","Romania","Romania","Romania","Romania","Romania","Romania","Romania","Romania","Romania","Romania","Russian Federation","Russian Federation","Russian Federation","Russian Federation","Russian Federation","Russian Federation","Russian Federation","Russian Federation","Russian Federation","Russian Federation","Russian Federation","Russian Federation","Russian Federation","Russian Federation","Russian Federation","Russian Federation","Russian Federation","Russian Federation","Russian Federation","Russian Federation","Russian Federation","Rwanda","Rwanda","Rwanda","Rwanda","Rwanda","Rwanda","Rwanda","Rwanda","Rwanda","Rwanda","Rwanda","Rwanda","Rwanda","Rwanda","Rwanda","Rwanda","Rwanda","Rwanda","Rwanda","Rwanda","Rwanda","Saint Lucia","Saint Lucia","Saint Lucia","Saint Lucia","Saint Lucia","Saint Lucia","Saint Lucia","Saint Lucia","Saint Lucia","Saint Lucia","Saint Lucia","Saint Lucia","Saint Lucia","Saint Lucia","Saint Lucia","Saint Lucia","Saint Lucia","Saint Lucia","Saint Lucia","Saint Lucia","Saint Lucia","St. Vincent and the Grenadines","St. Vincent and the Grenadines","St. Vincent and the Grenadines","St. Vincent and the Grenadines","St. Vincent and the Grenadines","St. Vincent and the Grenadines","St. Vincent and the Grenadines","St. Vincent and the Grenadines","St. Vincent and the Grenadines","St. Vincent and the Grenadines","St. Vincent and the Grenadines","St. Vincent and the Grenadines","St. Vincent and the Grenadines","St. Vincent and the Grenadines","St. Vincent and the Grenadines","St. Vincent and the Grenadines","St. Vincent and the Grenadines","St. Vincent and the Grenadines","St. Vincent and the Grenadines","St. Vincent and the Grenadines","St. Vincent and the Grenadines","Samoa","Samoa","Samoa","Samoa","Samoa","Samoa","Samoa","Samoa","Samoa","Samoa","Samoa","Samoa","Samoa","Samoa","Samoa","Samoa","Samoa","Samoa","Samoa","Samoa","Samoa","Sao Tome and Principe","Sao Tome and Principe","Sao Tome and Principe","Sao Tome and Principe","Sao Tome and Principe","Sao Tome and Principe","Sao Tome and Principe","Sao Tome and Principe","Sao Tome and Principe","Sao Tome and Principe","Sao Tome and Principe","Sao Tome and Principe","Sao Tome and Principe","Sao Tome and Principe","Sao Tome and Principe","Sao Tome and Principe","Sao Tome and Principe","Sao Tome and Principe","Sao Tome and Principe","Sao Tome and Principe","Sao Tome and Principe","Saudi Arabia","Saudi Arabia","Saudi Arabia","Saudi Arabia","Saudi Arabia","Saudi Arabia","Saudi Arabia","Saudi Arabia","Saudi Arabia","Saudi Arabia","Saudi Arabia","Saudi Arabia","Saudi Arabia","Saudi Arabia","Saudi Arabia","Saudi Arabia","Saudi Arabia","Saudi Arabia","Saudi Arabia","Saudi Arabia","Saudi Arabia","Senegal","Senegal","Senegal","Senegal","Senegal","Senegal","Senegal","Senegal","Senegal","Senegal","Senegal","Senegal","Senegal","Senegal","Senegal","Senegal","Senegal","Senegal","Senegal","Senegal","Senegal","Serbia","Serbia","Serbia","Serbia","Serbia","Serbia","Serbia","Serbia","Serbia","Serbia","Serbia","Serbia","Serbia","Serbia","Serbia","Serbia","Serbia","Serbia","Serbia","Serbia","Serbia","Seychelles","Seychelles","Seychelles","Seychelles","Seychelles","Seychelles","Seychelles","Seychelles","Seychelles","Seychelles","Seychelles","Seychelles","Seychelles","Seychelles","Seychelles","Seychelles","Seychelles","Seychelles","Seychelles","Seychelles","Seychelles","Sierra Leone","Sierra Leone","Sierra Leone","Sierra Leone","Sierra Leone","Sierra Leone","Sierra Leone","Sierra Leone","Sierra Leone","Sierra Leone","Sierra Leone","Sierra Leone","Sierra Leone","Sierra Leone","Sierra Leone","Sierra Leone","Sierra Leone","Sierra Leone","Sierra Leone","Sierra Leone","Sierra Leone","Singapore","Singapore","Singapore","Singapore","Singapore","Singapore","Singapore","Singapore","Singapore","Singapore","Singapore","Singapore","Singapore","Singapore","Singapore","Singapore","Singapore","Singapore","Singapore","Singapore","Singapore","Slovakia","Slovakia","Slovakia","Slovakia","Slovakia","Slovakia","Slovakia","Slovakia","Slovakia","Slovakia","Slovakia","Slovakia","Slovakia","Slovakia","Slovakia","Slovakia","Slovakia","Slovakia","Slovakia","Slovakia","Slovakia","Slovenia","Slovenia","Slovenia","Slovenia","Slovenia","Slovenia","Slovenia","Slovenia","Slovenia","Slovenia","Slovenia","Slovenia","Slovenia","Slovenia","Slovenia","Slovenia","Slovenia","Slovenia","Slovenia","Slovenia","Slovenia","Solomon Islands","Solomon Islands","Solomon Islands","Solomon Islands","Solomon Islands","Solomon Islands","Solomon Islands","Solomon Islands","Solomon Islands","Solomon Islands","Solomon Islands","Solomon Islands","Solomon Islands","Solomon Islands","Solomon Islands","Solomon Islands","Solomon Islands","Solomon Islands","Solomon Islands","Solomon Islands","Solomon Islands","Somalia","Somalia","Somalia","Somalia","Somalia","Somalia","Somalia","Somalia","Somalia","Somalia","Somalia","Somalia","Somalia","Somalia","Somalia","Somalia","Somalia","Somalia","Somalia","Somalia","Somalia","South Africa","South Africa","South Africa","South Africa","South Africa","South Africa","South Africa","South Africa","South Africa","South Africa","South Africa","South Africa","South Africa","South Africa","South Africa","South Africa","South Africa","South Africa","South Africa","South Africa","South Africa","South Sudan","South Sudan","South Sudan","South Sudan","South Sudan","South Sudan","South Sudan","South Sudan","South Sudan","South Sudan","South Sudan","South Sudan","South Sudan","South Sudan","South Sudan","South Sudan","South Sudan","South Sudan","South Sudan","South Sudan","South Sudan","Spain","Spain","Spain","Spain","Spain","Spain","Spain","Spain","Spain","Spain","Spain","Spain","Spain","Spain","Spain","Spain","Spain","Spain","Spain","Spain","Spain","Sri Lanka","Sri Lanka","Sri Lanka","Sri Lanka","Sri Lanka","Sri Lanka","Sri Lanka","Sri Lanka","Sri Lanka","Sri Lanka","Sri Lanka","Sri Lanka","Sri Lanka","Sri Lanka","Sri Lanka","Sri Lanka","Sri Lanka","Sri Lanka","Sri Lanka","Sri Lanka","Sri Lanka","Palestinian Territory, Occupied","Palestinian Territory, Occupied","Palestinian Territory, Occupied","Palestinian Territory, Occupied","Palestinian Territory, Occupied","Palestinian Territory, Occupied","Palestinian Territory, Occupied","Palestinian Territory, Occupied","Palestinian Territory, Occupied","Palestinian Territory, Occupied","Palestinian Territory, Occupied","Palestinian Territory, Occupied","Palestinian Territory, Occupied","Palestinian Territory, Occupied","Palestinian Territory, Occupied","Palestinian Territory, Occupied","Palestinian Territory, Occupied","Palestinian Territory, Occupied","Palestinian Territory, Occupied","Palestinian Territory, Occupied","Palestinian Territory, Occupied","Sudan","Sudan","Sudan","Sudan","Sudan","Sudan","Sudan","Sudan","Sudan","Sudan","Sudan","Sudan","Sudan","Sudan","Sudan","Sudan","Sudan","Sudan","Sudan","Sudan","Sudan","Suriname","Suriname","Suriname","Suriname","Suriname","Suriname","Suriname","Suriname","Suriname","Suriname","Suriname","Suriname","Suriname","Suriname","Suriname","Suriname","Suriname","Suriname","Suriname","Suriname","Suriname","Sweden","Sweden","Sweden","Sweden","Sweden","Sweden","Sweden","Sweden","Sweden","Sweden","Sweden","Sweden","Sweden","Sweden","Sweden","Sweden","Sweden","Sweden","Sweden","Sweden","Sweden","Switzerland","Switzerland","Switzerland","Switzerland","Switzerland","Switzerland","Switzerland","Switzerland","Switzerland","Switzerland","Switzerland","Switzerland","Switzerland","Switzerland","Switzerland","Switzerland","Switzerland","Switzerland","Switzerland","Switzerland","Switzerland","Syrian Arab Republic","Syrian Arab Republic","Syrian Arab Republic","Syrian Arab Republic","Syrian Arab Republic","Syrian Arab Republic","Syrian Arab Republic","Syrian Arab Republic","Syrian Arab Republic","Syrian Arab Republic","Syrian Arab Republic","Syrian Arab Republic","Syrian Arab Republic","Syrian Arab Republic","Syrian Arab Republic","Syrian Arab Republic","Syrian Arab Republic","Syrian Arab Republic","Syrian Arab Republic","Syrian Arab Republic","Syrian Arab Republic","Tajikistan","Tajikistan","Tajikistan","Tajikistan","Tajikistan","Tajikistan","Tajikistan","Tajikistan","Tajikistan","Tajikistan","Tajikistan","Tajikistan","Tajikistan","Tajikistan","Tajikistan","Tajikistan","Tajikistan","Tajikistan","Tajikistan","Tajikistan","Tajikistan","Thailand","Thailand","Thailand","Thailand","Thailand","Thailand","Thailand","Thailand","Thailand","Thailand","Thailand","Thailand","Thailand","Thailand","Thailand","Thailand","Thailand","Thailand","Thailand","Thailand","Thailand","Timor-Leste","Timor-Leste","Timor-Leste","Timor-Leste","Timor-Leste","Timor-Leste","Timor-Leste","Timor-Leste","Timor-Leste","Timor-Leste","Timor-Leste","Timor-Leste","Timor-Leste","Timor-Leste","Timor-Leste","Timor-Leste","Timor-Leste","Timor-Leste","Timor-Leste","Timor-Leste","Timor-Leste","Togo","Togo","Togo","Togo","Togo","Togo","Togo","Togo","Togo","Togo","Togo","Togo","Togo","Togo","Togo","Togo","Togo","Togo","Togo","Togo","Togo","Tonga","Tonga","Tonga","Tonga","Tonga","Tonga","Tonga","Tonga","Tonga","Tonga","Tonga","Tonga","Tonga","Tonga","Tonga","Tonga","Tonga","Tonga","Tonga","Tonga","Tonga","Trinidad and Tobago","Trinidad and Tobago","Trinidad and Tobago","Trinidad and Tobago","Trinidad and Tobago","Trinidad and Tobago","Trinidad and Tobago","Trinidad and Tobago","Trinidad and Tobago","Trinidad and Tobago","Trinidad and Tobago","Trinidad and Tobago","Trinidad and Tobago","Trinidad and Tobago","Trinidad and Tobago","Trinidad and Tobago","Trinidad and Tobago","Trinidad and Tobago","Trinidad and Tobago","Trinidad and Tobago","Trinidad and Tobago","Tunisia","Tunisia","Tunisia","Tunisia","Tunisia","Tunisia","Tunisia","Tunisia","Tunisia","Tunisia","Tunisia","Tunisia","Tunisia","Tunisia","Tunisia","Tunisia","Tunisia","Tunisia","Tunisia","Tunisia","Tunisia","Turkmenistan","Turkmenistan","Turkmenistan","Turkmenistan","Turkmenistan","Turkmenistan","Turkmenistan","Turkmenistan","Turkmenistan","Turkmenistan","Turkmenistan","Turkmenistan","Turkmenistan","Turkmenistan","Turkmenistan","Turkmenistan","Turkmenistan","Turkmenistan","Turkmenistan","Turkmenistan","Turkmenistan","Turkey","Turkey","Turkey","Turkey","Turkey","Turkey","Turkey","Turkey","Turkey","Turkey","Turkey","Turkey","Turkey","Turkey","Turkey","Turkey","Turkey","Turkey","Turkey","Turkey","Turkey","Uganda","Uganda","Uganda","Uganda","Uganda","Uganda","Uganda","Uganda","Uganda","Uganda","Uganda","Uganda","Uganda","Uganda","Uganda","Uganda","Uganda","Uganda","Uganda","Uganda","Uganda","Ukraine","Ukraine","Ukraine","Ukraine","Ukraine","Ukraine","Ukraine","Ukraine","Ukraine","Ukraine","Ukraine","Ukraine","Ukraine","Ukraine","Ukraine","Ukraine","Ukraine","Ukraine","Ukraine","Ukraine","Ukraine","United Arab Emirates","United Arab Emirates","United Arab Emirates","United Arab Emirates","United Arab Emirates","United Arab Emirates","United Arab Emirates","United Arab Emirates","United Arab Emirates","United Arab Emirates","United Arab Emirates","United Arab Emirates","United Arab Emirates","United Arab Emirates","United Arab Emirates","United Arab Emirates","United Arab Emirates","United Arab Emirates","United Arab Emirates","United Arab Emirates","United Arab Emirates","United Kingdom","United Kingdom","United Kingdom","United Kingdom","United Kingdom","United Kingdom","United Kingdom","United Kingdom","United Kingdom","United Kingdom","United Kingdom","United Kingdom","United Kingdom","United Kingdom","United Kingdom","United Kingdom","United Kingdom","United Kingdom","United Kingdom","United Kingdom","United Kingdom","Tanzania, United Republic of","Tanzania, United Republic of","Tanzania, United Republic of","Tanzania, United Republic of","Tanzania, United Republic of","Tanzania, United Republic of","Tanzania, United Republic of","Tanzania, United Republic of","Tanzania, United Republic of","Tanzania, United Republic of","Tanzania, United Republic of","Tanzania, United Republic of","Tanzania, United Republic of","Tanzania, United Republic of","Tanzania, United Republic of","Tanzania, United Republic of","Tanzania, United Republic of","Tanzania, United Republic of","Tanzania, United Republic of","Tanzania, United Republic of","Tanzania, United Republic of","United States","United States","United States","United States","United States","United States","United States","United States","United States","United States","United States","United States","United States","United States","United States","United States","United States","United States","United States","United States","United States","Uruguay","Uruguay","Uruguay","Uruguay","Uruguay","Uruguay","Uruguay","Uruguay","Uruguay","Uruguay","Uruguay","Uruguay","Uruguay","Uruguay","Uruguay","Uruguay","Uruguay","Uruguay","Uruguay","Uruguay","Uruguay","Uzbekistan","Uzbekistan","Uzbekistan","Uzbekistan","Uzbekistan","Uzbekistan","Uzbekistan","Uzbekistan","Uzbekistan","Uzbekistan","Uzbekistan","Uzbekistan","Uzbekistan","Uzbekistan","Uzbekistan","Uzbekistan","Uzbekistan","Uzbekistan","Uzbekistan","Uzbekistan","Uzbekistan","Vanuatu","Vanuatu","Vanuatu","Vanuatu","Vanuatu","Vanuatu","Vanuatu","Vanuatu","Vanuatu","Vanuatu","Vanuatu","Vanuatu","Vanuatu","Vanuatu","Vanuatu","Vanuatu","Vanuatu","Vanuatu","Vanuatu","Vanuatu","Vanuatu","Venezuela, Bolivarian Republic of","Venezuela, Bolivarian Republic of","Venezuela, Bolivarian Republic of","Venezuela, Bolivarian Republic of","Venezuela, Bolivarian Republic of","Venezuela, Bolivarian Republic of","Venezuela, Bolivarian Republic of","Venezuela, Bolivarian Republic of","Venezuela, Bolivarian Republic of","Venezuela, Bolivarian Republic of","Venezuela, Bolivarian Republic of","Venezuela, Bolivarian Republic of","Venezuela, Bolivarian Republic of","Venezuela, Bolivarian Republic of","Venezuela, Bolivarian Republic of","Venezuela, Bolivarian Republic of","Venezuela, Bolivarian Republic of","Venezuela, Bolivarian Republic of","Venezuela, Bolivarian Republic of","Venezuela, Bolivarian Republic of","Venezuela, Bolivarian Republic of","Vietnam","Vietnam","Vietnam","Vietnam","Vietnam","Vietnam","Vietnam","Vietnam","Vietnam","Vietnam","Vietnam","Vietnam","Vietnam","Vietnam","Vietnam","Vietnam","Vietnam","Vietnam","Vietnam","Vietnam","Vietnam","Yemen","Yemen","Yemen","Yemen","Yemen","Yemen","Yemen","Yemen","Yemen","Yemen","Yemen","Yemen","Yemen","Yemen","Yemen","Yemen","Yemen","Yemen","Yemen","Yemen","Yemen","Zambia","Zambia","Zambia","Zambia","Zambia","Zambia","Zambia","Zambia","Zambia","Zambia","Zambia","Zambia","Zambia","Zambia","Zambia","Zambia","Zambia","Zambia","Zambia","Zambia","Zambia","Zimbabwe","Zimbabwe","Zimbabwe","Zimbabwe","Zimbabwe","Zimbabwe","Zimbabwe","Zimbabwe","Zimbabwe","Zimbabwe","Zimbabwe","Zimbabwe","Zimbabwe","Zimbabwe","Zimbabwe","Zimbabwe","Zimbabwe","Zimbabwe","Zimbabwe","Zimbabwe","Zimbabwe"],"name":"","z":[13407.6,12339.5,12517.6,12714.4,12230.3,12119.9,11874.8,11841.8,10508.6,10308.2,10316.7,10233.4,10143.4,10242.2,10013.3,10208.1,9867.6,9081.7,8996.1,8878.1,8698.1,7.9,6.4,6.0,5.6,4.6,4.3,4.1,3.7,3.4,3.2,3.0,2.8,2.7,2.6,2.5,2.3,2.2,2.1,1.6,1.6,2.5,958.2,944.5,924.9,979.2,914.1,1003.2,983.1,963.0,943.8,970.3,981.1,957.6,938.2,905.7,848.6,895.8,904.2,908.4,802.9,763.3,757.5,6707.4,6437.1,6293.7,5784.0,5246.7,5014.5,4767.5,4472.3,4357.1,4076.6,3852.6,3595.0,3353.6,3293.0,3372.6,3231.2,3251.4,3112.0,2930.0,2923.5,2913.6,0.5,0.5,0.4,0.4,0.4,0.3,0.3,0.3,0.4,0.4,0.3,0.3,0.3,0.3,0.2,0.3,0.2,0.2,0.2,0.2,0.2,513.4,513.6,504.4,556.0,520.5,449.5,441.2,449.2,426.3,410.5,405.0,371.4,335.0,323.8,313.2,295.0,295.9,273.1,228.8,215.5,285.6,20.1,18.8,18.3,16.6,16.6,15.1,14.4,13.6,13.1,14.4,13.6,12.9,12.8,12.0,12.8,10.5,10.0,9.8,9.5,9.2,9.5,16.7,14.7,13.9,13.8,12.9,12.1,12.3,14.7,14.6,16.0,16.4,17.8,17.9,18.3,16.2,16.0,16.0,14.9,14.2,15.5,8.7,5.0,4.7,4.7,4.8,4.3,4.6,4.3,4.4,4.3,4.5,4.6,4.7,4.5,4.5,4.8,4.8,4.6,4.5,5.0,4.7,4.3,78.3,75.6,73.5,71.3,67.9,65.8,60.9,57.1,57.1,60.0,60.4,58.1,56.7,54.8,55.3,54.1,44.8,39.8,39.5,39.5,53.8,3.7,3.8,3.9,4.1,4.3,4.4,4.0,4.3,5.2,5.3,4.7,5.0,5.1,4.1,4.8,4.2,4.0,3.9,3.9,4.1,3.9,3.6,3.4,3.8,4.0,3.7,3.6,3.8,3.2,3.3,3.4,3.8,3.7,3.5,3.2,3.2,3.3,3.2,3.2,2.9,2.9,3.0,16531.2,16410.8,15546.1,15076.2,13741.5,13542.4,12440.8,13069.7,12433.2,11065.7,9556.8,9319.0,7247.7,6706.8,6678.2,6403.7,5956.9,5490.9,5207.1,4779.3,3719.1,1.9,1.9,1.9,1.8,1.7,1.7,1.7,1.6,1.6,1.6,1.6,1.6,1.6,1.5,1.5,1.5,1.4,1.4,1.4,1.4,1.2,24.1,22.3,15.6,12.7,10.1,10.2,7.9,6.0,4.7,3.7,3.0,2.9,2.3,2.0,1.8,1.6,1.5,1.4,1.1,1.0,1.0,9.6,9.2,8.9,8.4,8.1,8.1,7.9,8.3,7.9,7.8,7.6,7.3,6.6,6.9,6.5,6.3,6.0,5.8,5.8,5.3,5.5,6.0,6.0,5.3,5.4,5.6,5.0,4.5,3.9,3.2,2.7,2.3,2.3,2.3,2.5,3.1,3.9,4.7,5.8,6.3,6.0,9.1,1370.4,1440.0,1551.4,1599.7,1689.8,1695.6,1730.0,1708.9,1789.4,2124.7,2225.2,2344.9,2449.3,2456.0,2544.1,2523.0,2585.1,2555.4,2473.6,2416.2,2451.0,45.7,38.6,35.8,31.1,29.5,27.9,25.6,21.4,19.7,18.1,16.3,13.2,11.9,10.9,10.2,9.6,8.0,7.5,6.3,6.2,6.0,727.1,663.5,645.4,640.4,603.0,591.3,572.3,575.6,552.3,491.3,484.1,470.2,472.1,460.9,431.2,433.5,423.0,431.5,450.9,462.2,423.2,6.6,5.9,6.3,5.0,4.6,4.5,3.8,3.7,3.2,2.9,2.8,2.7,2.3,2.5,2.6,2.3,2.0,1.8,1.7,1.6,1.6,90.8,93.8,88.8,94.1,102.0,108.8,117.2,120.7,126.4,107.5,90.4,133.2,156.2,85.2,108.9,112.2,81.9,66.7,100.6,73.1,115.3,2386.5,2332.4,2426.1,2243.6,2272.5,2265.6,2269.5,2249.3,2165.4,2076.7,1942.5,1879.3,1698.9,1803.6,1869.7,1879.0,1821.9,1762.5,1757.7,1752.8,2010.8,3.0,3.0,3.1,2.8,2.8,2.8,2.8,2.9,2.9,2.9,2.9,3.0,3.0,3.0,3.1,3.1,3.1,3.2,3.1,2.7,2.7,15.8,14.5,12.8,11.7,11.0,10.2,9.1,8.2,7.4,8.2,8.0,6.1,5.4,5.1,5.1,5.0,4.7,4.6,4.5,4.2,4.3,2715.0,2742.9,2787.9,2643.3,2608.2,2559.7,2581.6,2610.0,2501.7,2512.5,2491.2,2423.7,2325.8,2387.3,2334.9,2213.8,2200.5,2129.0,2105.1,2178.2,2049.4,2350.1,2279.8,2276.0,2376.0,2381.4,2423.4,2469.2,2495.0,2419.3,2485.7,2590.1,2485.5,2452.8,2446.4,2342.9,2302.9,2196.5,2131.3,2195.9,2065.7,2150.8,16.3,13.4,12.5,10.6,9.6,9.2,8.7,7.9,8.3,6.9,5.9,5.5,5.9,4.7,4.7,5.1,4.6,4.4,4.8,4.2,4.2,2022.7,1905.5,1648.8,1534.4,1483.1,1275.1,1174.6,1118.6,1052.3,946.1,939.8,857.9,850.0,792.8,789.8,721.6,673.8,688.7,698.8,704.7,710.6,4034.5,3976.9,3980.9,3871.6,3856.0,4073.6,4064.2,3940.0,4053.1,4157.2,4187.6,4175.3,3969.8,4058.1,4020.6,3883.1,3913.4,4044.3,3904.1,4098.6,4119.3,30.1,32.0,33.7,35.0,35.3,38.1,38.1,38.4,47.6,47.4,44.5,44.4,44.7,43.2,44.2,43.3,46.2,47.0,40.6,40.5,40.9,2130.6,2118.1,2139.0,2159.1,2130.6,2084.4,2065.3,2113.8,2128.1,2176.5,2124.2,2119.7,2003.5,1984.4,1925.5,1809.3,1781.1,1889.8,1856.7,1855.6,1887.7,5789.7,5855.5,5731.1,5736.4,5910.1,6243.3,6486.4,6738.4,6797.2,7369.5,7559.0,7641.6,7568.9,7621.2,7343.4,7393.7,7593.7,7399.0,7436.3,7477.7,7763.5,79.7,82.7,76.1,75.7,66.2,62.4,67.2,67.2,61.8,58.6,56.8,48.8,45.5,43.2,38.5,38.3,34.4,32.6,33.6,32.7,34.3,10100.2,9111.2,8780.7,7026.7,8039.9,7597.1,7205.7,6796.7,6790.9,6158.1,5960.9,5737.1,5471.2,5166.0,4831.9,4533.0,4262.3,4030.6,3156.2,2985.0,2821.7,804.1,809.6,792.5,694.3,681.1,665.7,653.7,653.8,565.7,546.4,534.9,531.6,528.7,523.1,517.1,514.5,512.3,518.7,459.7,480.3,548.0,86.6,82.6,78.4,77.0,74.9,75.7,76.6,75.3,75.8,68.4,69.6,67.3,68.3,65.4,67.1,60.0,61.2,57.7,58.5,56.8,52.1,758.8,782.5,774.5,745.7,714.2,668.2,680.4,650.2,647.2,672.2,669.2,677.6,712.4,640.4,660.5,634.4,617.1,643.8,651.3,517.1,502.6,30.4,28.6,27.4,27.3,23.2,22.3,21.5,21.2,20.6,19.7,19.7,17.9,17.6,16.8,17.4,14.0,13.0,13.1,12.2,12.2,13.6,4.9,4.7,4.7,4.7,4.2,4.2,3.9,3.8,3.6,4.1,3.3,3.0,2.8,2.5,2.4,2.3,2.0,2.0,1.8,1.7,1.7,65.8,63.3,62.2,51.4,51.1,50.9,50.5,50.6,51.4,52.4,53.0,52.6,52.3,51.4,50.2,49.0,47.6,46.2,45.2,44.3,41.6,4.0,3.9,3.8,3.7,3.8,3.3,4.0,3.4,3.5,4.3,3.7,4.0,4.5,4.7,5.1,5.5,5.9,6.4,7.6,8.3,8.9,7.3,6.9,6.4,6.1,5.6,5.5,5.0,5.6,5.5,5.4,4.9,4.1,3.9,3.6,3.4,3.9,3.9,3.6,3.6,3.7,3.6,3565.2,3785.2,4013.0,4218.8,4208.2,4278.8,4638.8,4715.1,4745.0,5035.7,4972.1,4916.6,4975.2,4844.1,4633.4,4540.1,4680.5,4570.8,4663.8,4365.1,4400.7,755.5,687.3,715.5,446.8,470.1,426.6,449.4,468.2,476.1,442.8,408.9,378.4,349.4,316.5,286.1,370.6,373.0,371.4,370.8,368.4,368.1,14616.7,14836.2,15297.5,15525.9,15607.2,15864.4,16035.1,16812.7,17171.7,17291.8,17785.3,17953.9,18876.2,18980.8,19177.7,19835.9,19845.7,20795.9,20369.6,20757.6,21511.3,5.4,5.3,5.3,5.0,4.8,4.5,4.3,4.5,4.4,4.3,4.1,3.9,3.7,2.9,2.9,3.2,3.3,3.0,3.0,2.7,2.8,128.1,121.8,118.1,114.5,102.4,92.1,80.5,78.0,77.4,70.6,65.7,64.5,61.8,59.0,56.6,58.6,60.3,59.3,61.7,58.6,56.3,168.4,144.7,147.7,155.8,169.5,178.6,172.5,182.5,193.2,199.7,198.2,201.0,196.9,201.0,206.1,212.5,218.1,222.4,232.8,216.1,222.2,385.6,371.5,356.8,312.5,301.5,295.1,289.5,285.7,284.7,281.5,249.8,241.8,233.1,226.0,200.0,199.7,208.9,206.4,213.3,221.4,196.6,1529.3,1479.0,1427.6,1314.2,1259.8,1184.9,1103.8,1031.1,959.7,899.8,905.1,840.1,791.1,748.5,686.0,657.1,548.9,502.5,485.7,442.2,416.6,80.5,74.6,57.5,55.1,46.5,45.6,45.1,45.3,41.2,42.6,42.6,43.6,44.5,46.4,48.5,51.0,46.5,47.8,46.4,40.4,43.6,119.5,113.1,105.2,98.4,94.2,87.8,86.7,86.4,90.0,92.1,88.7,83.6,78.8,84.3,95.2,94.5,87.5,94.6,107.3,106.0,106.2,668.5,588.7,610.6,594.5,592.3,567.8,548.2,541.5,550.6,514.7,508.5,486.3,447.3,441.3,417.7,406.5,392.5,362.2,341.1,338.2,328.0,3.2,2.9,2.7,2.4,2.1,1.8,1.6,1.8,1.6,1.4,1.3,1.1,1.1,1.0,0.9,0.9,0.8,0.8,0.8,0.7,0.7,194.2,198.1,200.3,217.9,225.3,230.5,218.8,225.6,235.1,266.4,221.6,206.9,197.8,169.1,136.3,108.2,85.4,73.4,65.5,66.1,69.5,28432.6,29035.2,29630.4,28053.5,28253.9,27953.0,26110.0,25281.7,23516.8,22121.4,20685.3,19844.1,17869.8,16418.9,14968.5,13671.6,12473.1,12459.1,11438.7,11117.0,10246.2,9.8,9.8,10.3,10.0,9.7,9.5,9.3,9.3,9.1,8.9,8.7,7.8,7.8,7.8,7.7,7.8,7.5,7.0,7.0,6.9,6.8,4.3,4.1,4.1,3.9,4.2,4.4,3.9,4.2,4.1,4.4,4.3,4.1,4.3,4.3,3.9,4.0,4.1,3.6,3.7,3.9,3.8,72.0,71.3,70.6,69.4,67.6,67.2,77.4,65.4,77.0,77.2,73.9,72.4,70.4,68.3,67.2,57.1,56.2,54.4,55.4,54.2,53.9,106.9,104.7,104.8,100.5,104.4,114.9,116.9,119.1,114.1,114.4,109.9,110.7,106.6,118.1,133.9,133.7,136.0,139.4,146.3,144.3,142.7,482.2,478.6,502.0,508.0,506.5,502.9,503.2,516.8,507.1,504.7,495.8,483.2,476.8,502.3,456.4,454.7,429.5,419.6,434.9,407.9,398.7,27.5,22.2,21.0,20.6,24.6,22.7,22.1,22.7,22.9,24.6,23.8,22.3,20.4,18.8,16.9,17.8,14.5,14.3,14.2,13.5,13.5,54.4,52.0,51.3,49.7,47.5,46.6,35.7,43.7,43.5,43.0,41.6,40.2,37.6,37.0,34.0,34.0,39.3,37.1,36.7,34.4,33.7,3522.3,3378.9,3247.3,3155.2,3178.0,3059.6,2873.6,2813.4,2854.4,2775.1,2843.8,2742.9,2696.1,2735.6,2571.0,2617.7,2328.2,2399.3,2447.2,2197.0,2373.2,4.2,4.0,3.9,3.9,3.7,3.5,3.6,3.7,3.6,3.6,3.8,3.9,4.3,4.2,4.4,4.8,4.8,5.0,4.7,4.8,6.2,0.8,0.8,0.7,0.7,0.8,0.6,0.6,0.6,0.6,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.5,0.4,0.4,0.4,616.3,576.7,583.4,588.6,565.9,597.0,537.3,543.4,543.1,500.7,494.5,484.6,481.7,442.2,439.8,442.6,430.0,390.9,397.6,393.1,362.0,3388.5,3290.6,3231.4,3231.9,3185.1,3094.9,3049.0,2912.6,2873.5,2969.7,2999.8,3051.5,2818.4,2855.6,2841.1,2862.6,2791.2,2568.9,2560.4,2533.3,2556.7,676.1,637.7,613.6,605.1,564.4,556.9,507.4,498.4,504.6,482.1,476.7,475.7,477.6,474.7,468.8,456.0,424.1,444.5,408.4,447.0,464.1,38.0,36.1,32.8,32.4,30.9,30.9,30.1,28.6,25.4,24.6,23.7,22.7,21.8,21.2,21.0,20.5,20.3,19.7,18.8,18.7,17.9,1067.3,1100.4,1021.9,983.8,1132.9,961.8,911.7,974.5,1022.6,1060.3,1091.8,1150.1,1033.0,1050.7,1045.8,1055.9,1051.7,953.6,972.3,948.4,949.6,184.3,173.9,165.1,171.8,160.5,166.7,170.4,168.6,176.3,157.9,157.4,152.4,138.2,138.2,144.1,141.8,132.4,136.2,139.3,143.3,155.1,14.2,13.2,13.3,12.9,12.5,12.9,12.6,13.9,13.5,13.8,13.5,14.1,13.6,13.6,13.6,13.6,13.2,13.6,13.6,13.0,14.0,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.1,0.1,0.1,0.1,0.1,0.1,0.1,0.1,0.1,0.1,0.1,110009.7,107086.7,94379.4,89428.1,84649.2,78993.1,67573.6,63245.9,59297.9,55601.7,47527.5,44756.1,42100.4,39702.6,33578.3,31699.3,30029.3,28780.1,27965.1,27448.1,23753.1,13973.0,13283.8,13348.6,12508.8,13289.9,13105.6,12241.6,12370.2,12619.0,11849.6,10762.9,11875.8,10409.5,9524.5,9421.8,9282.1,9148.8,8990.0,8310.4,7211.0,7826.5,465.9,455.3,445.3,442.1,420.2,342.7,346.2,348.9,415.0,476.3,422.1,359.0,333.6,358.1,329.9,317.6,313.9,290.2,257.2,273.1,273.7,1041.9,1041.2,1028.5,1108.1,1140.8,1127.4,1220.6,1247.7,1268.9,1282.9,1230.3,1259.9,1287.4,1308.6,1196.2,1216.1,988.5,890.3,830.1,850.1,897.3,5.6,5.3,5.0,4.5,4.9,5.2,5.1,4.9,5.6,5.4,4.9,5.5,5.1,4.5,4.2,4.2,3.4,3.4,3.4,3.3,3.0,11.4,9.0,8.0,6.8,6.0,5.8,5.6,5.4,5.2,4.9,4.8,4.9,4.9,4.8,4.8,5.2,5.2,4.7,4.7,4.8,5.0,54.5,52.3,50.3,47.5,44.1,43.1,40.5,39.8,38.9,39.5,37.9,37.5,36.2,34.6,32.0,31.1,29.4,28.7,21.1,19.7,18.8,41.5,43.4,42.4,42.2,40.9,41.4,46.2,41.3,43.3,42.6,36.8,33.5,34.7,36.0,39.4,38.8,37.3,36.5,30.8,31.6,32.6,103.9,97.0,90.6,86.5,82.6,79.2,73.8,69.3,67.6,65.0,61.9,58.9,56.4,54.2,52.4,49.5,48.3,46.4,46.0,35.6,35.7,96.5,95.9,95.5,94.5,93.5,93.5,93.0,99.8,99.5,99.5,92.3,93.2,94.3,86.4,95.0,104.3,101.2,100.7,100.1,99.5,100.4,136.3,123.5,120.5,108.5,99.7,104.1,96.3,94.4,93.1,84.2,72.5,63.2,55.2,50.5,52.0,50.2,53.9,52.4,55.3,56.6,57.3,6945.5,7208.4,6961.7,6925.5,6790.2,6947.4,6976.1,7164.4,7112.4,6850.5,6994.6,6907.7,6921.0,7433.5,7278.3,7012.7,7353.1,7143.3,7468.0,7297.3,7716.3,3.5,3.6,3.4,3.4,3.5,3.5,3.5,3.5,3.8,3.8,3.9,3.9,3.9,3.6,3.6,3.6,3.5,3.3,3.3,3.2,3.1,4.2,4.3,4.5,4.5,4.7,4.8,5.0,5.1,5.6,5.9,5.6,5.3,4.7,4.5,4.7,4.3,3.7,3.6,3.9,4.0,3.8,92.9,92.5,92.3,92.9,98.0,99.2,97.4,110.1,107.2,102.7,109.7,104.7,101.4,108.4,100.3,103.0,88.4,86.8,91.2,79.2,81.1,1042.5,995.1,921.9,880.9,814.7,760.6,724.8,639.6,628.4,570.2,484.9,460.2,412.7,391.4,314.5,306.0,276.7,274.8,272.7,251.5,206.7,6.7,6.4,5.9,7.2,6.5,6.2,6.0,5.9,5.4,5.2,5.1,4.6,4.6,4.4,4.9,4.9,4.7,4.6,4.4,4.1,3.3,28.4,24.5,22.0,21.6,20.9,20.7,17.5,16.5,16.3,15.9,15.8,17.8,18.0,18.8,21.5,22.5,21.3,20.4,17.7,18.2,18.1,315.9,339.0,348.2,359.7,321.8,320.8,366.6,414.6,515.5,635.8,603.3,612.4,577.8,508.9,470.4,437.0,400.8,383.8,359.2,377.3,334.1,979.6,955.9,985.8,1054.7,902.7,899.7,936.9,974.3,954.8,969.8,970.3,997.5,1042.5,1010.6,1233.7,1083.2,997.8,1051.2,1094.0,1075.4,1050.3,61.8,68.4,68.9,66.3,65.3,69.1,73.4,78.0,74.6,82.1,87.9,98.5,84.5,91.2,90.0,93.2,95.1,85.0,86.3,89.2,88.0,6.3,6.0,4.5,4.0,3.7,3.5,4.2,3.8,3.5,3.2,3.0,2.7,2.6,2.5,2.7,2.7,2.5,2.4,2.3,2.1,2.3,0.6,0.6,0.6,0.6,0.5,0.5,0.6,0.5,0.5,0.5,0.5,0.4,0.5,0.5,0.4,0.4,0.4,0.4,0.4,0.4,0.4,4310.6,4170.8,4284.4,4285.6,4178.5,4057.9,3927.8,3885.4,4000.5,3934.8,3889.9,3797.9,3746.0,3614.0,3743.1,3920.5,3735.4,3597.6,3648.6,3471.4,3464.9,2924.7,2760.7,2606.4,2430.5,2158.0,1987.9,1902.7,2070.7,2488.5,2843.8,3082.7,2994.2,3038.7,2868.7,2680.1,2696.3,2607.9,2301.8,2440.9,2347.3,2451.5,209.5,180.0,175.8,152.7,150.7,146.9,145.9,128.9,145.7,144.1,124.1,121.0,119.8,119.6,119.2,118.6,115.2,112.8,111.2,110.3,108.0,6.9,5.8,5.0,4.8,4.7,4.7,4.6,4.6,4.8,4.8,4.8,4.8,4.1,3.9,3.9,4.0,4.1,3.7,3.9,4.0,4.0,3934.4,3754.3,3528.2,3447.7,3437.9,3546.9,3562.0,3799.7,4006.4,3901.6,3958.5,4063.3,4231.6,4196.3,4087.0,3969.8,3850.8,3798.6,3762.5,3738.7,3926.8,0.4,0.4,0.4,0.4,0.3,0.3,0.3,0.3,0.3,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.2,0.1,697.3,684.7,704.7,719.0,716.2,730.4,752.4,746.2,767.6,726.3,738.5,729.8,736.3,714.9,734.9,708.9,676.6,654.4,673.3,638.0,695.7,10.4,10.0,9.7,9.4,9.1,9.1,7.7,7.7,7.7,7.9,8.3,6.4,7.0,6.7,7.1,7.4,6.7,6.4,6.5,6.4,11.0,1339.2,1339.5,1337.2,1218.0,1223.8,1233.6,1249.5,1276.6,1295.1,1168.9,1161.9,1143.6,1119.1,1108.7,1101.9,1123.3,1038.5,1089.7,1133.9,1139.1,1159.4,2.4,2.1,2.7,1.9,1.9,1.7,1.7,1.6,1.5,1.4,1.4,1.4,1.3,1.3,1.2,1.3,1.3,1.3,1.4,1.3,1.5,78.9,70.8,65.3,51.1,47.4,45.1,48.2,45.0,47.3,44.1,41.3,40.5,40.9,38.9,37.6,36.8,36.3,36.1,31.7,29.8,29.2,1.1,0.9,0.8,0.8,0.8,0.8,0.8,0.7,0.8,0.8,0.6,0.6,0.6,0.5,0.5,0.5,0.5,0.4,0.4,0.4,0.4,1587.4,1523.3,1463.9,1399.0,1354.8,1266.3,1182.7,1112.9,1048.8,990.1,931.7,863.0,804.7,759.1,719.0,680.9,583.4,551.2,528.1,508.5,472.1,4145.1,3965.9,3713.5,3638.8,3502.0,3421.3,3350.4,3318.9,3409.0,3345.3,3118.9,2931.1,2729.4,2466.9,2460.9,2351.5,2062.1,1930.9,1780.5,1697.1,1465.6,3885.0,3421.8,3421.5,3328.8,3365.0,3263.0,3331.3,3179.5,2849.0,2727.7,2810.0,2651.9,2683.2,2519.2,2469.5,2302.3,2301.9,2257.2,2020.9,1997.7,1658.1,256.7,251.9,250.0,252.5,225.0,238.8,243.8,252.0,264.1,284.8,308.2,273.3,242.5,227.0,211.3,209.3,172.4,159.5,152.6,156.1,148.1,3800.0,3577.6,3372.0,3147.2,2769.4,2613.3,2383.5,2304.8,2188.3,2114.9,2154.6,1810.7,1769.5,1598.6,1554.6,1538.5,1358.7,1345.7,1206.9,1097.6,1051.7,26.6,25.2,25.1,23.4,21.2,19.5,17.0,15.3,14.2,13.0,11.5,11.7,10.7,9.8,9.5,8.9,9.0,8.5,6.7,6.7,7.5,6.3,6.2,5.5,5.7,6.6,5.7,6.4,6.5,6.1,6.3,6.2,6.3,5.8,4.6,4.5,5.2,4.5,4.5,4.5,4.5,4.4,239.7,245.0,229.9,231.3,228.4,217.4,186.2,174.3,157.2,146.1,138.9,134.2,131.7,130.2,116.4,114.3,111.2,108.7,106.4,106.6,109.8,5304.7,5521.8,5625.5,5729.9,5473.1,5390.4,5290.9,5218.0,5124.9,5051.6,4798.4,4778.9,4770.3,4707.8,4643.3,4597.1,4558.4,4365.1,4501.1,4407.8,4895.9,61336.4,61937.0,62772.8,62634.9,64222.5,64967.5,66297.3,68472.5,71529.0,73154.4,76072.2,73983.9,76272.5,78682.1,81615.2,80977.8,83378.9,84371.7,86177.9,86380.3,81747.2,3.3,3.0,3.0,2.8,2.2,2.0,1.9,1.8,1.6,1.7,1.6,1.2,1.2,1.0,1.1,1.0,0.8,0.7,0.6,0.6,0.6,3.4,3.0,2.8,3.0,3.2,3.1,3.0,2.9,2.7,2.6,2.5,2.3,1.9,1.8,1.5,1.4,1.3,1.2,1.1,1.0,0.9,11.5,11.4,12.2,10.9,11.2,10.7,11.1,11.7,11.9,12.4,11.6,12.1,12.6,13.1,13.3,13.3,13.2,14.0,14.6,14.0,14.8,21320.9,20989.7,20479.0,19903.9,19112.8,17269.1,15595.1,15039.2,14504.4,14876.2,14409.9,13738.7,13858.5,13259.5,13371.2,11803.4,11827.8,11109.6,11200.4,11349.5,9809.5,46.5,45.1,44.7,44.4,43.6,39.5,39.8,40.1,40.6,41.0,42.3,42.0,42.1,41.0,39.8,38.6,38.4,39.0,36.7,39.3,38.1,583.2,609.6,644.3,667.9,638.1,662.1,691.1,731.7,647.3,653.7,664.5,613.8,605.0,559.0,554.9,506.4,513.9,520.3,497.7,476.4,485.4,206.4,202.7,179.3,174.6,169.1,167.9,149.9,145.6,140.3,136.3,131.6,129.1,111.4,108.3,105.2,111.2,96.3,96.1,97.7,97.1,98.9,717.1,654.8,629.7,603.0,632.3,614.7,574.5,552.4,523.7,499.1,472.0,450.3,431.7,421.1,382.1,375.9,354.9,350.3,362.8,425.5,406.4,2896.8,3118.4,2904.9,2900.0,2914.0,2852.0,2865.0,2780.0,2568.1,2566.0,2538.1,2531.2,2489.0,2507.5,2158.3,2109.4,2066.6,2034.9,2005.5,1983.5,1934.8,29.6,26.0,22.8,20.6,19.3,17.8,16.4,15.0,13.6,12.4,10.7,10.2,9.4,8.7,8.4,8.0,7.7,7.7,7.4,7.2,7.3,12.9,10.7,10.3,10.1,9.6,9.8,9.1,9.5,9.5,9.8,10.0,9.2,9.3,7.2,7.2,8.8,9.2,9.6,9.6,9.6,9.8,13.3,12.8,12.5,10.5,10.2,10.0,9.8,9.5,9.3,9.2,8.9,8.6,7.0,6.7,6.4,5.8,5.3,4.2,4.1,5.4,9.3,3.4,3.0,3.3,3.2,3.0,2.5,2.0,1.9,2.0,1.9,1.8,2.0,2.1,1.9,1.7,1.7,1.6,1.7,1.8,2.0,2.4,91.1,82.2,80.0,62.1,57.7,53.7,49.2,46.5,42.2,39.1,37.3,44.1,42.0,30.6,27.8,26.4,24.3,22.3,21.1,19.5,23.9,24.5,21.4,19.3,16.7,14.4,15.4,13.6,12.2,11.0,10.0,9.6,9.0,8.6,8.1,8.9,8.2,7.2,6.5,6.1,4.8,4.8,113.0,103.6,101.7,105.0,100.4,84.0,69.9,58.2,57.0,51.6,50.4,38.7,36.8,33.2,31.5,30.7,33.5,27.7,24.1,21.1,20.0,680.9,601.5,690.8,619.9,532.0,473.7,408.9,358.8,324.3,343.4,313.0,265.1,237.0,211.5,193.0,203.3,160.1,147.7,140.9,110.8,197.2,3361.8,3015.0,2772.8,2459.6,2101.5,1901.4,1737.8,1682.1,1563.9,1448.1,1385.0,1309.8,1169.4,1164.5,1120.6,1156.7,1102.4,1054.7,1100.1,1111.2,1033.1,2.6,2.4,2.0,2.0,1.7,1.6,1.6,1.6,1.6,1.6,1.5,1.5,1.5,1.5,1.4,1.6,1.3,1.3,1.2,1.4,1.5,1.5,1.3,1.2,1.2,1.1,1.1,1.0,0.9,0.8,0.9,0.9,0.9,0.9,0.9,0.8,0.7,0.7,0.7,0.6,0.7,0.6,4.5,4.4,4.0,3.8,3.7,3.7,3.5,3.5,3.5,3.7,3.7,3.5,3.8,3.5,3.6,3.5,3.4,3.5,3.5,4.0,3.5,10.8,10.9,10.2,10.0,9.5,9.6,9.7,10.4,10.5,11.0,11.2,12.8,11.2,11.1,10.1,9.7,9.9,8.6,8.9,8.5,8.8,128.3,122.9,121.8,113.4,102.0,94.8,99.4,105.4,101.4,106.2,98.3,99.7,99.8,93.2,97.1,101.1,102.8,105.9,109.6,116.5,107.9,2432.2,2307.4,2361.4,2281.8,2259.3,2193.7,2135.5,2107.2,2213.7,2196.0,2133.4,2020.6,1941.7,1772.0,1756.5,1629.9,1435.4,1444.0,1467.9,1380.8,1416.6,13.5,12.3,12.2,11.7,11.3,11.1,10.3,10.2,10.1,10.1,10.1,9.9,9.7,9.2,9.1,9.0,8.5,8.4,7.9,7.3,7.0,0.4,0.4,0.4,0.3,0.3,0.3,0.3,0.3,0.2,0.2,0.2,0.2,0.1,0.1,0.1,0.1,0.1,0.1,0.1,0.1,0.1,3432.2,3413.8,3373.4,3350.9,3184.9,3145.9,2951.7,2722.5,2392.7,2234.6,2093.4,1840.8,1700.5,1605.6,1570.5,1488.6,1287.5,1342.3,1194.7,1140.3,1164.6,8.2,6.8,6.6,6.5,6.1,5.6,5.4,5.3,5.2,4.0,3.9,3.7,4.4,3.4,4.1,3.9,3.0,2.8,2.7,2.5,3.1,4.7,4.8,4.4,4.3,4.1,4.1,3.6,4.0,3.4,3.3,3.1,3.1,2.9,3.0,2.9,2.7,2.9,2.8,2.7,2.8,2.7,2.1,1.6,1.5,1.5,1.7,1.7,1.5,1.4,1.3,1.5,1.4,1.3,1.3,1.2,1.1,1.1,1.0,0.9,0.9,0.7,0.9,22.5,23.5,24.3,25.1,25.4,24.5,24.9,26.4,25.8,26.3,26.5,26.7,27.0,27.7,28.0,28.2,26.5,26.7,26.7,26.7,25.7,4760.7,4878.4,5076.6,5273.8,5485.7,5540.2,5630.4,5726.1,5633.9,5372.7,5547.9,5534.8,5091.1,5002.8,4929.7,4870.0,4670.5,4611.9,4509.2,4310.4,4518.6,1678.3,1620.6,1846.6,2017.6,2393.4,2369.8,2314.2,2466.2,2625.8,2610.8,2525.8,2262.8,1951.6,1802.4,1700.3,1669.9,1460.9,1561.2,1519.8,1461.8,1515.7,5278.9,5326.2,5486.3,4632.6,4528.5,4408.5,4307.3,4036.6,4052.7,4146.9,4069.7,4343.1,4526.0,4919.7,5167.8,5009.1,5151.7,4493.3,4053.9,3772.9,3789.8,20.1,20.3,20.1,21.5,20.5,20.6,20.4,20.3,20.6,20.3,19.1,19.2,18.5,17.6,17.1,16.2,15.6,15.4,14.9,11.2,12.1,208.9,194.7,188.2,181.5,176.0,163.3,155.7,150.4,148.6,143.6,135.3,131.9,126.4,120.4,105.3,103.3,99.3,100.1,96.9,93.9,89.4,75.1,78.6,78.1,74.2,74.5,67.9,68.0,63.6,63.4,62.2,58.7,55.6,49.1,45.0,43.0,38.7,35.9,31.4,30.4,29.3,29.6,6447.5,6512.7,6463.0,6240.1,5913.9,5578.7,5527.6,5134.7,5418.4,4883.3,4876.6,4520.0,4221.1,4233.4,4042.6,4146.3,4274.5,4194.0,4333.3,4487.7,4112.1,33.4,32.8,31.2,30.0,27.5,22.8,21.2,19.9,18.6,16.9,15.2,14.4,14.4,14.7,14.9,13.7,11.6,10.9,10.7,11.0,10.6,5.5,5.3,5.4,5.5,5.3,5.2,5.5,5.4,5.5,5.5,5.2,5.4,5.6,5.6,5.5,5.1,5.2,5.2,5.2,5.2,5.0,6.1,6.2,6.6,6.3,6.4,6.8,6.5,6.2,6.2,6.0,6.4,6.5,6.0,5.9,5.6,5.6,7.0,5.3,6.5,6.1,6.4,168.5,152.1,138.4,128.3,137.0,133.2,124.3,128.3,146.7,131.8,136.5,149.3,158.1,163.5,137.1,121.0,103.6,108.4,108.4,123.9,121.5,135.0,119.9,109.6,96.0,91.3,87.7,82.8,80.7,76.4,71.1,75.6,69.8,65.9,61.0,57.1,54.4,52.3,46.9,45.5,43.2,43.7,410.7,404.6,329.1,329.4,350.2,330.8,313.2,314.2,308.9,299.5,287.6,275.3,261.2,248.8,236.2,224.7,210.1,203.1,197.9,192.9,187.6,262.4,257.5,246.5,233.9,224.7,204.4,191.6,170.0,157.8,145.6,127.9,121.8,109.6,105.1,96.2,94.2,86.6,84.5,82.3,73.8,67.3,929.9,947.5,936.2,947.1,1028.2,1063.1,1143.5,1180.2,1230.5,1243.1,1304.5,1234.5,1266.5,1238.4,1248.0,1132.9,1145.3,1123.1,1160.2,1129.3,1089.4,2.8,2.9,2.8,2.8,2.8,2.8,3.0,2.9,2.9,3.1,2.8,2.8,2.8,2.8,2.8,2.6,2.5,2.5,2.5,2.5,2.5,14.8,13.3,11.6,12.9,11.3,11.2,11.8,11.3,11.4,9.5,9.8,9.3,8.5,7.7,7.0,6.2,5.9,5.4,5.2,5.0,4.8,103.4,103.4,102.4,101.4,100.4,99.0,97.2,95.4,93.2,89.7,87.4,96.2,93.4,91.1,89.6,88.0,83.1,82.8,82.7,82.8,74.0,28.2,26.5,22.6,20.7,18.9,18.3,16.4,14.9,13.4,13.1,11.7,10.6,10.6,9.8,9.2,8.6,8.5,7.3,7.3,7.0,7.2,435.9,426.6,374.0,361.9,344.4,330.0,317.6,306.0,297.9,290.1,286.6,296.0,279.1,270.9,272.1,276.4,281.2,241.3,230.6,221.6,219.3,5394.5,5419.6,5525.0,5580.9,5623.1,5611.7,5448.5,5070.5,5251.9,5370.2,5196.7,5080.3,4798.2,4497.7,4844.1,4711.0,4654.7,4808.6,4476.5,4712.9,4699.7,137.2,120.7,108.9,102.4,92.6,88.6,104.2,99.7,95.9,88.0,84.3,76.2,86.8,83.2,60.0,53.6,47.3,44.0,43.4,32.8,56.1,11.5,10.4,10.4,8.2,8.3,8.4,7.8,8.4,9.2,10.0,10.6,10.8,9.6,9.6,9.6,9.6,8.3,8.2,8.3,8.5,9.2,74.2,73.9,76.7,78.6,78.8,79.3,81.2,81.5,82.6,79.3,76.4,72.8,67.2,65.3,65.8,65.5,66.2,64.5,67.3,65.4,66.8,11044.0,10573.7,10251.0,9783.0,9485.3,9297.1,9272.6,9730.2,10569.1,9861.4,8722.3,8318.4,7215.7,7244.7,6964.0,6696.4,6207.0,6000.0,5819.4,5823.6,5390.3,481.9,507.1,520.9,540.6,540.6,553.3,564.4,571.5,595.8,639.6,568.2,608.4,630.1,651.1,672.0,694.4,730.0,740.8,739.6,745.9,773.8,13.8,12.0,11.6,11.2,10.7,10.2,9.7,9.5,9.1,8.8,8.5,8.4,8.1,8.0,8.1,8.1,8.2,7.1,7.2,7.4,6.5,236.3,221.6,226.7,230.0,231.2,248.6,250.7,247.8,244.7,246.6,244.8,239.5,235.3,229.7,224.0,221.9,220.2,216.6,239.5,239.6,251.1,6.5,6.9,6.7,6.8,6.8,6.8,6.8,6.9,6.9,7.0,7.4,7.6,7.8,7.8,8.3,8.3,8.5,8.5,8.7,8.3,8.5,539.7,628.8,585.2,641.2,631.9,568.4,573.0,582.3,630.6,656.2,671.0,705.4,704.6,736.8,702.4,738.3,878.4,1001.7,975.6,877.3,1207.8,1389.3,1208.4,1198.3,1173.6,1147.4,1137.4,1137.4,1152.3,1190.5,1240.1,1295.0,1350.7,1437.2,1522.0,1602.4,1689.9,1776.8,1874.8,1959.3,2006.3,1848.9,2065.1,2004.6,1833.1,1734.1,1665.0,1591.5,1521.3,1411.5,1443.6,1352.9,1387.9,1404.2,1453.6,1417.5,1491.6,1586.8,1678.8,1764.2,1747.5,1818.8,1852.3,1900.9,1668.1,1584.3,1482.4,1546.0,1580.3,1610.0,1591.7,1764.1,1842.0,1546.5,1366.4,1312.8,1151.9,1024.8,1017.6,969.4,986.4,931.5,840.0,891.5,1644.1,2539.3,1917.0,2322.5,2118.3,2292.2,2383.4,2862.0,3074.9,3141.8,2955.6,2737.5,2585.3,2436.7,2151.4,1967.1,1918.8,1762.3,1735.2,1906.9,1733.8],"type":"choropleth"}],                        {"template":{"data":{"histogram2dcontour":[{"type":"histogram2dcontour","colorbar":{"outlinewidth":0,"ticks":""},"colorscale":[[0.0,"#0d0887"],[0.1111111111111111,"#46039f"],[0.2222222222222222,"#7201a8"],[0.3333333333333333,"#9c179e"],[0.4444444444444444,"#bd3786"],[0.5555555555555556,"#d8576b"],[0.6666666666666666,"#ed7953"],[0.7777777777777778,"#fb9f3a"],[0.8888888888888888,"#fdca26"],[1.0,"#f0f921"]]}],"choropleth":[{"type":"choropleth","colorbar":{"outlinewidth":0,"ticks":""}}],"histogram2d":[{"type":"histogram2d","colorbar":{"outlinewidth":0,"ticks":""},"colorscale":[[0.0,"#0d0887"],[0.1111111111111111,"#46039f"],[0.2222222222222222,"#7201a8"],[0.3333333333333333,"#9c179e"],[0.4444444444444444,"#bd3786"],[0.5555555555555556,"#d8576b"],[0.6666666666666666,"#ed7953"],[0.7777777777777778,"#fb9f3a"],[0.8888888888888888,"#fdca26"],[1.0,"#f0f921"]]}],"heatmap":[{"type":"heatmap","colorbar":{"outlinewidth":0,"ticks":""},"colorscale":[[0.0,"#0d0887"],[0.1111111111111111,"#46039f"],[0.2222222222222222,"#7201a8"],[0.3333333333333333,"#9c179e"],[0.4444444444444444,"#bd3786"],[0.5555555555555556,"#d8576b"],[0.6666666666666666,"#ed7953"],[0.7777777777777778,"#fb9f3a"],[0.8888888888888888,"#fdca26"],[1.0,"#f0f921"]]}],"heatmapgl":[{"type":"heatmapgl","colorbar":{"outlinewidth":0,"ticks":""},"colorscale":[[0.0,"#0d0887"],[0.1111111111111111,"#46039f"],[0.2222222222222222,"#7201a8"],[0.3333333333333333,"#9c179e"],[0.4444444444444444,"#bd3786"],[0.5555555555555556,"#d8576b"],[0.6666666666666666,"#ed7953"],[0.7777777777777778,"#fb9f3a"],[0.8888888888888888,"#fdca26"],[1.0,"#f0f921"]]}],"contourcarpet":[{"type":"contourcarpet","colorbar":{"outlinewidth":0,"ticks":""}}],"contour":[{"type":"contour","colorbar":{"outlinewidth":0,"ticks":""},"colorscale":[[0.0,"#0d0887"],[0.1111111111111111,"#46039f"],[0.2222222222222222,"#7201a8"],[0.3333333333333333,"#9c179e"],[0.4444444444444444,"#bd3786"],[0.5555555555555556,"#d8576b"],[0.6666666666666666,"#ed7953"],[0.7777777777777778,"#fb9f3a"],[0.8888888888888888,"#fdca26"],[1.0,"#f0f921"]]}],"surface":[{"type":"surface","colorbar":{"outlinewidth":0,"ticks":""},"colorscale":[[0.0,"#0d0887"],[0.1111111111111111,"#46039f"],[0.2222222222222222,"#7201a8"],[0.3333333333333333,"#9c179e"],[0.4444444444444444,"#bd3786"],[0.5555555555555556,"#d8576b"],[0.6666666666666666,"#ed7953"],[0.7777777777777778,"#fb9f3a"],[0.8888888888888888,"#fdca26"],[1.0,"#f0f921"]]}],"mesh3d":[{"type":"mesh3d","colorbar":{"outlinewidth":0,"ticks":""}}],"scatter":[{"fillpattern":{"fillmode":"overlay","size":10,"solidity":0.2},"type":"scatter"}],"parcoords":[{"type":"parcoords","line":{"colorbar":{"outlinewidth":0,"ticks":""}}}],"scatterpolargl":[{"type":"scatterpolargl","marker":{"colorbar":{"outlinewidth":0,"ticks":""}}}],"bar":[{"error_x":{"color":"#2a3f5f"},"error_y":{"color":"#2a3f5f"},"marker":{"line":{"color":"#E5ECF6","width":0.5},"pattern":{"fillmode":"overlay","size":10,"solidity":0.2}},"type":"bar"}],"scattergeo":[{"type":"scattergeo","marker":{"colorbar":{"outlinewidth":0,"ticks":""}}}],"scatterpolar":[{"type":"scatterpolar","marker":{"colorbar":{"outlinewidth":0,"ticks":""}}}],"histogram":[{"marker":{"pattern":{"fillmode":"overlay","size":10,"solidity":0.2}},"type":"histogram"}],"scattergl":[{"type":"scattergl","marker":{"colorbar":{"outlinewidth":0,"ticks":""}}}],"scatter3d":[{"type":"scatter3d","line":{"colorbar":{"outlinewidth":0,"ticks":""}},"marker":{"colorbar":{"outlinewidth":0,"ticks":""}}}],"scattermapbox":[{"type":"scattermapbox","marker":{"colorbar":{"outlinewidth":0,"ticks":""}}}],"scatterternary":[{"type":"scatterternary","marker":{"colorbar":{"outlinewidth":0,"ticks":""}}}],"scattercarpet":[{"type":"scattercarpet","marker":{"colorbar":{"outlinewidth":0,"ticks":""}}}],"carpet":[{"aaxis":{"endlinecolor":"#2a3f5f","gridcolor":"white","linecolor":"white","minorgridcolor":"white","startlinecolor":"#2a3f5f"},"baxis":{"endlinecolor":"#2a3f5f","gridcolor":"white","linecolor":"white","minorgridcolor":"white","startlinecolor":"#2a3f5f"},"type":"carpet"}],"table":[{"cells":{"fill":{"color":"#EBF0F8"},"line":{"color":"white"}},"header":{"fill":{"color":"#C8D4E3"},"line":{"color":"white"}},"type":"table"}],"barpolar":[{"marker":{"line":{"color":"#E5ECF6","width":0.5},"pattern":{"fillmode":"overlay","size":10,"solidity":0.2}},"type":"barpolar"}],"pie":[{"automargin":true,"type":"pie"}]},"layout":{"autotypenumbers":"strict","colorway":["#636efa","#EF553B","#00cc96","#ab63fa","#FFA15A","#19d3f3","#FF6692","#B6E880","#FF97FF","#FECB52"],"font":{"color":"#2a3f5f"},"hovermode":"closest","hoverlabel":{"align":"left"},"paper_bgcolor":"white","plot_bgcolor":"#E5ECF6","polar":{"bgcolor":"#E5ECF6","angularaxis":{"gridcolor":"white","linecolor":"white","ticks":""},"radialaxis":{"gridcolor":"white","linecolor":"white","ticks":""}},"ternary":{"bgcolor":"#E5ECF6","aaxis":{"gridcolor":"white","linecolor":"white","ticks":""},"baxis":{"gridcolor":"white","linecolor":"white","ticks":""},"caxis":{"gridcolor":"white","linecolor":"white","ticks":""}},"coloraxis":{"colorbar":{"outlinewidth":0,"ticks":""}},"colorscale":{"sequential":[[0.0,"#0d0887"],[0.1111111111111111,"#46039f"],[0.2222222222222222,"#7201a8"],[0.3333333333333333,"#9c179e"],[0.4444444444444444,"#bd3786"],[0.5555555555555556,"#d8576b"],[0.6666666666666666,"#ed7953"],[0.7777777777777778,"#fb9f3a"],[0.8888888888888888,"#fdca26"],[1.0,"#f0f921"]],"sequentialminus":[[0.0,"#0d0887"],[0.1111111111111111,"#46039f"],[0.2222222222222222,"#7201a8"],[0.3333333333333333,"#9c179e"],[0.4444444444444444,"#bd3786"],[0.5555555555555556,"#d8576b"],[0.6666666666666666,"#ed7953"],[0.7777777777777778,"#fb9f3a"],[0.8888888888888888,"#fdca26"],[1.0,"#f0f921"]],"diverging":[[0,"#8e0152"],[0.1,"#c51b7d"],[0.2,"#de77ae"],[0.3,"#f1b6da"],[0.4,"#fde0ef"],[0.5,"#f7f7f7"],[0.6,"#e6f5d0"],[0.7,"#b8e186"],[0.8,"#7fbc41"],[0.9,"#4d9221"],[1,"#276419"]]},"xaxis":{"gridcolor":"white","linecolor":"white","ticks":"","title":{"standoff":15},"zerolinecolor":"white","automargin":true,"zerolinewidth":2},"yaxis":{"gridcolor":"white","linecolor":"white","ticks":"","title":{"standoff":15},"zerolinecolor":"white","automargin":true,"zerolinewidth":2},"scene":{"xaxis":{"backgroundcolor":"#E5ECF6","gridcolor":"white","linecolor":"white","showbackground":true,"ticks":"","zerolinecolor":"white","gridwidth":2},"yaxis":{"backgroundcolor":"#E5ECF6","gridcolor":"white","linecolor":"white","showbackground":true,"ticks":"","zerolinecolor":"white","gridwidth":2},"zaxis":{"backgroundcolor":"#E5ECF6","gridcolor":"white","linecolor":"white","showbackground":true,"ticks":"","zerolinecolor":"white","gridwidth":2}},"shapedefaults":{"line":{"color":"#2a3f5f"}},"annotationdefaults":{"arrowcolor":"#2a3f5f","arrowhead":0,"arrowwidth":1},"geo":{"bgcolor":"white","landcolor":"#E5ECF6","subunitcolor":"white","showland":true,"showlakes":true,"lakecolor":"white"},"title":{"x":0.05},"mapbox":{"style":"light"}}},"geo":{"domain":{"x":[0.0,1.0],"y":[0.0,1.0]},"center":{},"showframe":false,"showcoastlines":false},"coloraxis":{"colorbar":{"title":{"text":"obs_value"}},"colorscale":[[0.0,"#440154"],[0.1111111111111111,"#482878"],[0.2222222222222222,"#3e4989"],[0.3333333333333333,"#31688e"],[0.4444444444444444,"#26828e"],[0.5555555555555556,"#1f9e89"],[0.6666666666666666,"#35b779"],[0.7777777777777778,"#6ece58"],[0.8888888888888888,"#b5de2b"],[1.0,"#fde725"]]},"legend":{"tracegroupgap":0},"title":{"text":"Global Visualization of Observation Values by Country"}},                        {"responsive": true}                    ).then(function(){
                            
var gd = document.getElementById('902eff77-8c93-417a-8acb-44b69e167d64');
var x = new MutationObserver(function (mutations, observer) {{
        var display = window.getComputedStyle(gd).display;
        if (!display || display === 'none') {{
            console.log([gd, 'removed!']);
            Plotly.purge(gd);
            observer.disconnect();
        }}
}});

// Listen for the removal of the full notebook cells
var notebookContainer = gd.closest('#notebook-container');
if (notebookContainer) {{
    x.observe(notebookContainer, {childList: true});
}}

// Listen for the clearing of the current output cell
var outputEl = gd.closest('.output');
if (outputEl) {{
    x.observe(outputEl, {childList: true});
}}

                        })                };                            </script>        </div>


</div>
</div>

</main>
<!-- /main column -->
<script id="quarto-html-after-body" type="application/javascript">
window.document.addEventListener("DOMContentLoaded", function (event) {
  const toggleBodyColorMode = (bsSheetEl) => {
    const mode = bsSheetEl.getAttribute("data-mode");
    const bodyEl = window.document.querySelector("body");
    if (mode === "dark") {
      bodyEl.classList.add("quarto-dark");
      bodyEl.classList.remove("quarto-light");
    } else {
      bodyEl.classList.add("quarto-light");
      bodyEl.classList.remove("quarto-dark");
    }
  }
  const toggleBodyColorPrimary = () => {
    const bsSheetEl = window.document.querySelector("link#quarto-bootstrap");
    if (bsSheetEl) {
      toggleBodyColorMode(bsSheetEl);
    }
  }
  toggleBodyColorPrimary();  
  const icon = "";
  const anchorJS = new window.AnchorJS();
  anchorJS.options = {
    placement: 'right',
    icon: icon
  };
  anchorJS.add('.anchored');
  const isCodeAnnotation = (el) => {
    for (const clz of el.classList) {
      if (clz.startsWith('code-annotation-')) {                     
        return true;
      }
    }
    return false;
  }
  const onCopySuccess = function(e) {
    // button target
    const button = e.trigger;
    // don't keep focus
    button.blur();
    // flash "checked"
    button.classList.add('code-copy-button-checked');
    var currentTitle = button.getAttribute("title");
    button.setAttribute("title", "Copied!");
    let tooltip;
    if (window.bootstrap) {
      button.setAttribute("data-bs-toggle", "tooltip");
      button.setAttribute("data-bs-placement", "left");
      button.setAttribute("data-bs-title", "Copied!");
      tooltip = new bootstrap.Tooltip(button, 
        { trigger: "manual", 
          customClass: "code-copy-button-tooltip",
          offset: [0, -8]});
      tooltip.show();    
    }
    setTimeout(function() {
      if (tooltip) {
        tooltip.hide();
        button.removeAttribute("data-bs-title");
        button.removeAttribute("data-bs-toggle");
        button.removeAttribute("data-bs-placement");
      }
      button.setAttribute("title", currentTitle);
      button.classList.remove('code-copy-button-checked');
    }, 1000);
    // clear code selection
    e.clearSelection();
  }
  const getTextToCopy = function(trigger) {
      const codeEl = trigger.previousElementSibling.cloneNode(true);
      for (const childEl of codeEl.children) {
        if (isCodeAnnotation(childEl)) {
          childEl.remove();
        }
      }
      return codeEl.innerText;
  }
  const clipboard = new window.ClipboardJS('.code-copy-button:not([data-in-quarto-modal])', {
    text: getTextToCopy
  });
  clipboard.on('success', onCopySuccess);
  if (window.document.getElementById('quarto-embedded-source-code-modal')) {
    const clipboardModal = new window.ClipboardJS('.code-copy-button[data-in-quarto-modal]', {
      text: getTextToCopy,
      container: window.document.getElementById('quarto-embedded-source-code-modal')
    });
    clipboardModal.on('success', onCopySuccess);
  }
    var localhostRegex = new RegExp(/^(?:http|https):\/\/localhost\:?[0-9]*\//);
    var mailtoRegex = new RegExp(/^mailto:/);
      var filterRegex = new RegExp('/' + window.location.host + '/');
    var isInternal = (href) => {
        return filterRegex.test(href) || localhostRegex.test(href) || mailtoRegex.test(href);
    }
    // Inspect non-navigation links and adorn them if external
 	var links = window.document.querySelectorAll('a[href]:not(.nav-link):not(.navbar-brand):not(.toc-action):not(.sidebar-link):not(.sidebar-item-toggle):not(.pagination-link):not(.no-external):not([aria-hidden]):not(.dropdown-item):not(.quarto-navigation-tool):not(.about-link)');
    for (var i=0; i<links.length; i++) {
      const link = links[i];
      if (!isInternal(link.href)) {
        // undo the damage that might have been done by quarto-nav.js in the case of
        // links that we want to consider external
        if (link.dataset.originalHref !== undefined) {
          link.href = link.dataset.originalHref;
        }
      }
    }
  function tippyHover(el, contentFn, onTriggerFn, onUntriggerFn) {
    const config = {
      allowHTML: true,
      maxWidth: 500,
      delay: 100,
      arrow: false,
      appendTo: function(el) {
          return el.parentElement;
      },
      interactive: true,
      interactiveBorder: 10,
      theme: 'quarto',
      placement: 'bottom-start',
    };
    if (contentFn) {
      config.content = contentFn;
    }
    if (onTriggerFn) {
      config.onTrigger = onTriggerFn;
    }
    if (onUntriggerFn) {
      config.onUntrigger = onUntriggerFn;
    }
    window.tippy(el, config); 
  }
  const noterefs = window.document.querySelectorAll('a[role="doc-noteref"]');
  for (var i=0; i<noterefs.length; i++) {
    const ref = noterefs[i];
    tippyHover(ref, function() {
      // use id or data attribute instead here
      let href = ref.getAttribute('data-footnote-href') || ref.getAttribute('href');
      try { href = new URL(href).hash; } catch {}
      const id = href.replace(/^#\/?/, "");
      const note = window.document.getElementById(id);
      if (note) {
        return note.innerHTML;
      } else {
        return "";
      }
    });
  }
  const xrefs = window.document.querySelectorAll('a.quarto-xref');
  const processXRef = (id, note) => {
    // Strip column container classes
    const stripColumnClz = (el) => {
      el.classList.remove("page-full", "page-columns");
      if (el.children) {
        for (const child of el.children) {
          stripColumnClz(child);
        }
      }
    }
    stripColumnClz(note)
    if (id === null || id.startsWith('sec-')) {
      // Special case sections, only their first couple elements
      const container = document.createElement("div");
      if (note.children && note.children.length > 2) {
        container.appendChild(note.children[0].cloneNode(true));
        for (let i = 1; i < note.children.length; i++) {
          const child = note.children[i];
          if (child.tagName === "P" && child.innerText === "") {
            continue;
          } else {
            container.appendChild(child.cloneNode(true));
            break;
          }
        }
        if (window.Quarto?.typesetMath) {
          window.Quarto.typesetMath(container);
        }
        return container.innerHTML
      } else {
        if (window.Quarto?.typesetMath) {
          window.Quarto.typesetMath(note);
        }
        return note.innerHTML;
      }
    } else {
      // Remove any anchor links if they are present
      const anchorLink = note.querySelector('a.anchorjs-link');
      if (anchorLink) {
        anchorLink.remove();
      }
      if (window.Quarto?.typesetMath) {
        window.Quarto.typesetMath(note);
      }
      if (note.classList.contains("callout")) {
        return note.outerHTML;
      } else {
        return note.innerHTML;
      }
    }
  }
  for (var i=0; i<xrefs.length; i++) {
    const xref = xrefs[i];
    tippyHover(xref, undefined, function(instance) {
      instance.disable();
      let url = xref.getAttribute('href');
      let hash = undefined; 
      if (url.startsWith('#')) {
        hash = url;
      } else {
        try { hash = new URL(url).hash; } catch {}
      }
      if (hash) {
        const id = hash.replace(/^#\/?/, "");
        const note = window.document.getElementById(id);
        if (note !== null) {
          try {
            const html = processXRef(id, note.cloneNode(true));
            instance.setContent(html);
          } finally {
            instance.enable();
            instance.show();
          }
        } else {
          // See if we can fetch this
          fetch(url.split('#')[0])
          .then(res => res.text())
          .then(html => {
            const parser = new DOMParser();
            const htmlDoc = parser.parseFromString(html, "text/html");
            const note = htmlDoc.getElementById(id);
            if (note !== null) {
              const html = processXRef(id, note);
              instance.setContent(html);
            } 
          }).finally(() => {
            instance.enable();
            instance.show();
          });
        }
      } else {
        // See if we can fetch a full url (with no hash to target)
        // This is a special case and we should probably do some content thinning / targeting
        fetch(url)
        .then(res => res.text())
        .then(html => {
          const parser = new DOMParser();
          const htmlDoc = parser.parseFromString(html, "text/html");
          const note = htmlDoc.querySelector('main.content');
          if (note !== null) {
            // This should only happen for chapter cross references
            // (since there is no id in the URL)
            // remove the first header
            if (note.children.length > 0 && note.children[0].tagName === "HEADER") {
              note.children[0].remove();
            }
            const html = processXRef(null, note);
            instance.setContent(html);
          } 
        }).finally(() => {
          instance.enable();
          instance.show();
        });
      }
    }, function(instance) {
    });
  }
      let selectedAnnoteEl;
      const selectorForAnnotation = ( cell, annotation) => {
        let cellAttr = 'data-code-cell="' + cell + '"';
        let lineAttr = 'data-code-annotation="' +  annotation + '"';
        const selector = 'span[' + cellAttr + '][' + lineAttr + ']';
        return selector;
      }
      const selectCodeLines = (annoteEl) => {
        const doc = window.document;
        const targetCell = annoteEl.getAttribute("data-target-cell");
        const targetAnnotation = annoteEl.getAttribute("data-target-annotation");
        const annoteSpan = window.document.querySelector(selectorForAnnotation(targetCell, targetAnnotation));
        const lines = annoteSpan.getAttribute("data-code-lines").split(",");
        const lineIds = lines.map((line) => {
          return targetCell + "-" + line;
        })
        let top = null;
        let height = null;
        let parent = null;
        if (lineIds.length > 0) {
            //compute the position of the single el (top and bottom and make a div)
            const el = window.document.getElementById(lineIds[0]);
            top = el.offsetTop;
            height = el.offsetHeight;
            parent = el.parentElement.parentElement;
          if (lineIds.length > 1) {
            const lastEl = window.document.getElementById(lineIds[lineIds.length - 1]);
            const bottom = lastEl.offsetTop + lastEl.offsetHeight;
            height = bottom - top;
          }
          if (top !== null && height !== null && parent !== null) {
            // cook up a div (if necessary) and position it 
            let div = window.document.getElementById("code-annotation-line-highlight");
            if (div === null) {
              div = window.document.createElement("div");
              div.setAttribute("id", "code-annotation-line-highlight");
              div.style.position = 'absolute';
              parent.appendChild(div);
            }
            div.style.top = top - 2 + "px";
            div.style.height = height + 4 + "px";
            div.style.left = 0;
            let gutterDiv = window.document.getElementById("code-annotation-line-highlight-gutter");
            if (gutterDiv === null) {
              gutterDiv = window.document.createElement("div");
              gutterDiv.setAttribute("id", "code-annotation-line-highlight-gutter");
              gutterDiv.style.position = 'absolute';
              const codeCell = window.document.getElementById(targetCell);
              const gutter = codeCell.querySelector('.code-annotation-gutter');
              gutter.appendChild(gutterDiv);
            }
            gutterDiv.style.top = top - 2 + "px";
            gutterDiv.style.height = height + 4 + "px";
          }
          selectedAnnoteEl = annoteEl;
        }
      };
      const unselectCodeLines = () => {
        const elementsIds = ["code-annotation-line-highlight", "code-annotation-line-highlight-gutter"];
        elementsIds.forEach((elId) => {
          const div = window.document.getElementById(elId);
          if (div) {
            div.remove();
          }
        });
        selectedAnnoteEl = undefined;
      };
        // Handle positioning of the toggle
    window.addEventListener(
      "resize",
      throttle(() => {
        elRect = undefined;
        if (selectedAnnoteEl) {
          selectCodeLines(selectedAnnoteEl);
        }
      }, 10)
    );
    function throttle(fn, ms) {
    let throttle = false;
    let timer;
      return (...args) => {
        if(!throttle) { // first call gets through
            fn.apply(this, args);
            throttle = true;
        } else { // all the others get throttled
            if(timer) clearTimeout(timer); // cancel #2
            timer = setTimeout(() => {
              fn.apply(this, args);
              timer = throttle = false;
            }, ms);
        }
      };
    }
      // Attach click handler to the DT
      const annoteDls = window.document.querySelectorAll('dt[data-target-cell]');
      for (const annoteDlNode of annoteDls) {
        annoteDlNode.addEventListener('click', (event) => {
          const clickedEl = event.target;
          if (clickedEl !== selectedAnnoteEl) {
            unselectCodeLines();
            const activeEl = window.document.querySelector('dt[data-target-cell].code-annotation-active');
            if (activeEl) {
              activeEl.classList.remove('code-annotation-active');
            }
            selectCodeLines(clickedEl);
            clickedEl.classList.add('code-annotation-active');
          } else {
            // Unselect the line
            unselectCodeLines();
            clickedEl.classList.remove('code-annotation-active');
          }
        });
      }
  const findCites = (el) => {
    const parentEl = el.parentElement;
    if (parentEl) {
      const cites = parentEl.dataset.cites;
      if (cites) {
        return {
          el,
          cites: cites.split(' ')
        };
      } else {
        return findCites(el.parentElement)
      }
    } else {
      return undefined;
    }
  };
  var bibliorefs = window.document.querySelectorAll('a[role="doc-biblioref"]');
  for (var i=0; i<bibliorefs.length; i++) {
    const ref = bibliorefs[i];
    const citeInfo = findCites(ref);
    if (citeInfo) {
      tippyHover(citeInfo.el, function() {
        var popup = window.document.createElement('div');
        citeInfo.cites.forEach(function(cite) {
          var citeDiv = window.document.createElement('div');
          citeDiv.classList.add('hanging-indent');
          citeDiv.classList.add('csl-entry');
          var biblioDiv = window.document.getElementById('ref-' + cite);
          if (biblioDiv) {
            citeDiv.innerHTML = biblioDiv.innerHTML;
          }
          popup.appendChild(citeDiv);
        });
        return popup.innerHTML;
      });
    }
  }
});
</script>
</div> <!-- /content -->




</body></html>

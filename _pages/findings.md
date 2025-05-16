---
title: "Findings"
layout: splash
permalink: /findings
# header:
#     overlay_color: "rgba(7, 165, 7, 0.3)"
#     overlay_filter: "0.1"
    # overlay_image: {{ site.baseurl }}/assets/overview.png
# excerpt: "Multi-Dimensional Evaluation of LLM Reasoning in Anesthesiology"
model_scale:
  - image_path: {{ site.baseurl }}/assets/updated1_models_en.png
    alt: "Model Scale Analysis"
    title: "<div style=\"margin: auto;\">Model Scale Analysis on AnesBench</div>"
    excerpt: "<div style=\"max-width: 900px;width: 100%;margin: auto auto 20px auto;padding: 10px 20px;background: linear-gradient(135deg, #f0fff0, #e6ffe6);border: 3px solid #90ee90;border-radius: 12px;box-shadow: 0 4px 20px rgba(0, 128, 0, 0.1);min-height: 300px;display: flex;flex-direction: column;justify-content: center;font-family: 'Segoe UI', sans-serif;line-height: 1.6;color: #333;\"><div style=\"font-size: 1.4em; font-weight: bold; margin-bottom: 10px; color: #2e8b57;\">📌 Conclusion 1.1:</div><div style=\"font-size: 1.1em; margin-bottom: 20px;\">Model performance is strongly positively correlated with model scale, yet this relationship exhibits diminishing marginal returns.</div><div style=\"font-size: 1.4em; font-weight: bold; margin-bottom: 10px; color: #2e8b57;\">📌 Conclusion 1.2:</div><div style=\"font-size: 1.1em;\">Compared to System 1, the performance gains achieved by increasing model scale on System 2 are significantly lower.</div></div>"
  - image_path: {{ site.baseurl }}/assets/updated1_models_cn.png
    alt: "Model Scale Analysis"
    title: "<div style=\"margin: auto;\">Model Scale Analysis on AMCQA</div>"
    excerpt: "<div style=\"max-width: 900px;width: 100%;margin: auto auto 20px auto;padding: 10px 20px;background: linear-gradient(135deg, #f0fff0, #e6ffe6);border: 3px solid #90ee90;border-radius: 12px;box-shadow: 0 4px 20px rgba(0, 128, 0, 0.1);min-height: 300px;display: flex;flex-direction: column;justify-content: center;font-family: 'Segoe UI', sans-serif;line-height: 1.6;color: #333;\"><div style=\"font-size: 1.4em; font-weight: bold; margin-bottom: 10px; color: #2e8b57;\">📌 Conclusion 1.3:</div><div style=\"font-size: 1.1em; margin-bottom: 20px;\">Consistent with findings on AnesBench, Chinese AMCQA also demonstrates a positive correlation between model performance and scale, exhibiting diminishing returns. However, the distinction between system1,system1.x and system2 is not pronounced, potentially due to dataset's limited differentiation in difficulty levels.</div></div>"
language:
  - image_path: {{ site.baseurl }}/assets/translation_lollipop.png
    alt: "Language Transferability Analysis"
    title: "<div style=\"margin: auto;\">Language Transferability Analysis</div>"
    excerpt: "<div style=\"text-align: left;max-width: 900px;width: 100%;margin: auto auto 20px auto;padding: 10px 20px;background: linear-gradient(135deg, #f0fff0, #e6ffe6);border: 3px solid #90ee90;border-radius: 12px;box-shadow: 0 4px 20px rgba(0, 128, 0, 0.1);min-height: 300px;display: flex;flex-direction: column;justify-content: center;font-family: 'Segoe UI', sans-serif;line-height: 1.6;color: #333;\"><div style=\"font-size: 1.4em; font-weight: bold; margin-bottom: 10px; color: #2e8b57;\">📌 Conclusion 1.4:</div><div style=\"font-size: 1.1em; margin-bottom: 20px;\">Language transfer ability remains critical for multilingual model performance in anesthesia reasoning. We recommend continued pre-training to address the deficiency in domain-specific knowledge across languages at the stable language ability stage.</div></div>"
distillation:
  - image_path: {{ site.baseurl }}/assets/impact_of_r1_distillation.png
    alt: "Distillation Analysis"
    title: "<div style=\"margin: auto;\">Distillation Analysis</div>"
    excerpt: "<div style=\"text-align: left;max-width: 900px;width: 100%;margin: auto auto 20px auto;padding: 10px 20px;background: linear-gradient(135deg, #f0fff0, #e6ffe6);border: 3px solid #90ee90;border-radius: 12px;box-shadow: 0 4px 20px rgba(0, 128, 0, 0.1);min-height: 300px;display: flex;flex-direction: column;justify-content: center;font-family: 'Segoe UI', sans-serif;line-height: 1.6;color: #333;\"><div style=\"font-size: 1.4em; font-weight: bold; margin-bottom: 10px; color: #2e8b57;\">📌 Conclusion 2.3:</div><div style=\"font-size: 1.1em; margin-bottom: 20px;\">Reasoning skills distilled from diverse tasks transfer well to niche domains, suggesting reasoning is more generalizable than domain knowledge.</div><div style=\"font-size: 1.4em; font-weight: bold; margin-bottom: 10px; color: #2e8b57;\">📌 Conclusion 2.4:</div><div style=\"font-size: 1.1em; margin-bottom: 20px;\">Larger models better absorb complex reasoning, highlighting the key role of model capacity in learning structured thinking.</div></div>"
#   - image_path: /assets/images/unsplash-gallery-image-2-th.jpg
#     alt: "placeholder image 2"
#     title: "Placeholder 2"
#     excerpt: "This is some sample content that goes here with **Markdown** formatting."
#     url: "#test-link"
#     btn_label: "Read More"
#     btn_class: "btn--inverse"

classes:
    - wide
---



# 😼 Impact of Model Characteristics

---
## Model Scale
{% include feature_row id="model_scale" type="left" %}

## Language Transferability
{% include feature_row id="language" type="right" %}

## Model's CoT Length
<div class="feature__wrapper">
  <div class="feature__item--left">
    <div class="archive__item" style="display: flex; flex-direction: row; gap: 20px; align-items: flex-start;">
      <div class="archive__item-teaser" style="flex-shrink: 0; max-width: 960px; width: 100%;">
        <img src="{{ site.baseurl }}/anesbench.ai/assets/models_length.png" alt="Model CoT Length Analysis" style="width: 100%; border-radius: 8px;">
      </div>
      <div class="archive__item-body" style="flex: 1; min-width: 0;">
        <h2 class="archive__item-title" style="margin: 0 0 10px 0; text-align: left;">
          CoT Length Analysis
        </h2>
        <div class="archive__item-excerpt">
          <div style="width: 100%;padding: 16px 24px;background: linear-gradient(135deg, #f0fff0, #e6ffe6);border: 3px solid #90ee90;border-radius: 12px;box-shadow: 0 4px 20px rgba(0, 128, 0, 0.1);min-height: 100px;display: flex;flex-direction: column;justify-content: center;font-family: 'Segoe UI', sans-serif;line-height: 1.6;color: #333;">
            <div style="font-size: 1.4em; font-weight: bold; margin-bottom: 10px; color: #2e8b57;">📌 Conclusion 1.5:</div><div style="font-size: 1.1em; margin-bottom: 20px;">Models that achieve superior performance on System2 questions often engage in longer CoT reasoning processes.</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

# 😺 Impact of Training Strategies and Reasoning Techniques

## Training Strategies
<div class="feature__wrapper">
  <div class="feature__item--left">
    <div class="archive__item" style="display: flex; flex-direction: row; gap: 20px; align-items: flex-start;">
      <div class="archive__item-teaser" style="flex-shrink: 0; max-width: 800px; width: 100%;">
      <style>table td {
  line-height: 1.7;
}</style>
    <table style="table-layout: auto; width: 100%; max-width: 800px; border-collapse: collapse;display: table !important;">
 <thead>
            <tr>
              <th style="text-align: center;" rowspan="2">Model</th>
              <th style="text-align: center;" colspan="2">SFT Data</th>
              <th style="text-align: center;">Accuracy</th>
            </tr>
            <tr>
              <th style="text-align: center;">AnesQA</th>
              <th style="text-align: center;">Medical-o1</th>
              <th style="text-align: center;">ANESBENCH</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td style="text-align: center;">Qwen2.5-7B-Instruct</td>
              <td style="text-align: center;">-</td>
              <td style="text-align: center;">-</td>
              <td style="text-align: center;">51.5</td>
            </tr>
            <tr>
              <td style="text-align: center;" rowspan="3">Qwen2.5-7B-Base</td>
              <td style="text-align: center;">✓</td>
              <td style="text-align: center;">X</td>
              <td style="text-align: center;">49.3</td>
            </tr>
            <tr>
              <td style="text-align: center;">X</td>
              <td style="text-align: center;">✓</td>
              <td style="text-align: center;">49.1</td>
            </tr>
            <tr>
              <td style="text-align: center;">✓</td>
              <td style="text-align: center;">✓</td>
              <td style="text-align: center;">49.7</td>
            </tr>
            <tr>
              <td style="text-align: center;" rowspan="3">Qwen2.5-7B-Base-CPT</td>
              <td style="text-align: center;">✓</td>
              <td style="text-align: center;">X</td>
              <td style="text-align: center;">49.7</td>
            </tr>
            <tr>
              <td style="text-align: center;">X</td>
              <td style="text-align: center;">✓</td>
              <td style="text-align: center;">50.7</td>
            </tr>
            <tr>
              <td style="text-align: center;">✓</td>
              <td style="text-align: center;">✓</td>
              <td style="text-align: center;">51.2</td>
            </tr>
          </tbody>
    </table>
      </div>
      <div class="archive__item-body" style="flex: 1; min-width: 100px; max-height: 800px; height: 100%">
        <h2 class="archive__item-title" style="margin: 10px 0 0px 0; text-align: left;">
          Training Strategies Analysis
        </h2>
        <div class="archive__item-excerpt">
          <div style="width: 100%;padding: 16px 24px;min-height: 100px;background: linear-gradient(135deg, #f0fff0, #e6ffe6);border: 3px solid #90ee90;border-radius: 12px;box-shadow: 0 4px 20px rgba(0, 128, 0, 0.1);display: flex;flex-direction: column;justify-content: center;font-family: 'Segoe UI', sans-serif;line-height: 1.6;color: #333;">
            <div style="font-size: 1.4em; font-weight: bold; margin-bottom: 10px; color: #2e8b57;">📌 Conclusion 2.1:</div><div style="font-size: 1.1em; margin-bottom: 20px;">Continuous pre-training (CPT), by adapting models to domain-specific data prior to fine-tuning, yields significant performance gains.</div>
            <div style="font-size: 1.4em; font-weight: bold; margin-bottom: 10px; color: #2e8b57;">📌 Conclusion 2.2:</div><div style="font-size: 1.1em; margin-bottom: 20px;">Combining factual and problem-solving data reveals that strong reasoning relies on both declarative and procedural knowledge.</div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>

## R1 Distillation
{% include feature_row id="distillation" type="right" %}

## Reasoning Strategies

<div class="feature__wrapper">
  <div class="feature__item--left">
    <div class="archive__item" style="display: flex; flex-direction: row; gap: 20px; align-items: flex-start;">
      <div class="archive__item-teaser" style="flex-shrink: 0; max-width: 800px; width: 100%;">
      <style>table td {
  line-height: 1.8;
}</style>
    <table style="table-layout: auto; width: 100%; max-width: 800px; border-collapse: collapse;display: table !important;">
      <thead>
            <tr>
              <th style="text-align: center;">Reasoning Strategy</th>
              <th style="text-align: center;">Tree Width</th>
              <th style="text-align: center;">Beam Size</th>
              <th style="text-align: center;">Step Tokens</th>
              <th style="text-align: center;">Accuracy(%)</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td style="text-align: center;">None</td>
              <td style="text-align: center;">-</td>
              <td style="text-align: center;">-</td>
              <td style="text-align: center;">-</td>
              <td style="text-align: center;">51.2</td>
            </tr>
            <tr>
              <td style="text-align: center;" rowspan="2">Best-of-N [21]</td>
              <td style="text-align: center;">4</td>
              <td style="text-align: center;">-</td>
              <td style="text-align: center;">-</td>
              <td style="text-align: center;">51.5</td>
            </tr>
            <tr>
              <td style="text-align: center;">8</td>
              <td style="text-align: center;">-</td>
              <td style="text-align: center;">-</td>
              <td style="text-align: center;">51.5</td>
            </tr>
            <tr>
              <td style="text-align: center;" rowspan="2">Beam Search [19]</td>
              <td style="text-align: center;">4</td>
              <td style="text-align: center;">4</td>
              <td style="text-align: center;">32</td>
              <td style="text-align: center;">52.1</td>
            </tr>
            <tr>
              <td style="text-align: center;">8</td>
              <td style="text-align: center;">8</td>
              <td style="text-align: center;">32</td>
              <td style="text-align: center;"><strong>52.4</strong></td>
            </tr>
          </tbody>
    </table>
      </div>
      <div class="archive__item-body" style="flex: 1; min-width: 100px; max-height: 800px; height: 100%">
        <h2 class="archive__item-title" style="margin: 20px 0 0px 0; text-align: left;">
          Reasoning Strategies Analysis
        </h2>
        <div class="archive__item-excerpt">
          <div style="width: 100%;padding: 16px 24px;min-height: 100px;height: 100%;background: linear-gradient(135deg, #f0fff0, #e6ffe6);border: 3px solid #90ee90;border-radius: 12px;box-shadow: 0 4px 20px rgba(0, 128, 0, 0.1);display: flex;flex-direction: column;justify-content: center;font-family: 'Segoe UI', sans-serif;line-height: 1.6;color: #333;">
            <div style="font-size: 1.4em; font-weight: bold; margin-bottom: 10px; color: #2e8b57;">📌 Conclusion 2.5:</div><div style="font-size: 1.1em; margin-bottom: 20px;">Test-time strategies that invest more compute to explore alternative reasoning paths can yield meaningful performance gains. </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>





<!-- # 😼 Impact of Model Characteristics


<div style="display: flex; flex-wrap: wrap; justify-content: center; gap: 15px;">
  <div style="flex: 0 1 45%; min-width: 700px; margin-bottom: 40px;">
    <figure style="position: relative;">
      <img src="{{ site.baseurl }}/assets/updated1_models_cn.png" alt="Model Scale Analysis" style="width: 100%;">
      <figcaption style="position: absolute; top: 110%; left: 50%; transform: translate(-50%, -50%); text-align: left;">
        <div style="min-width: 1000px; border: 2px solid #98ff98; border-radius: 10px; padding: 15px; margin: 10px auto; max-width: 600px; background-color: rgba(240, 255, 240, 0.7);">
          <b style="font-size: 1.2em;">Conclusion 1:</b> <b style="font-size: 1.05em;">Model performance is strongly positively correlated with model scale, yet this relationship exhibits diminishing marginal returns.</b><br>
          <b style="font-size: 1.2em;">Conclusion 2:</b> <b style="font-size: 1.05em;">Compared to System 1, the performance gains achieved by increasing model scale on System 2 are significantly lower.</b>
        </div>
      </figcaption>
    </figure>
  </div>

  <div style="flex: 0 1 45%; min-width: 700px; margin-bottom: 40px;">
    <figure style="position: relative;">
      <img src="{{ site.baseurl }}/assets/updated1_models_en.png" alt="Model Scale Analysis" style="width: 100%;">
      <figcaption style="position: absolute; top: 110%; left: 50%; transform: translate(-50%, -50%); text-align: left;">
        <div style="min-width: 1000px; border: 2px solid #98ff98; border-radius: 10px; padding: 15px; margin: 10px auto; max-width: 600px; background-color: rgba(240, 255, 240, 0.7);">
          <b style="font-size: 1.2em;">Conclusion 3:</b> <b style="font-size: 1.05em;">Consistent with findings on AnesBench, Chinese AMCQA also demonstrates a positive correlation between model performance and scale, exhibiting diminishing returns. However, the distinction between system1,system1.x and system2 is not pronounced, potentially due to dataset's limited differentiation in difficulty levels.</b><br>
        </div>
      </figcaption>
    </figure>
  </div>

  <div style="flex: 0 1 45%; min-width: 700px; margin-bottom: 40px;">
    <figure style="position: relative;">
      <img src="{{ site.baseurl }}/assets/translation_lollipop.png" alt="Model Scale Analysis" style="width: 100%;">
      <figcaption style="position: absolute; top: 110%; left: 50%; transform: translate(-50%, -50%); text-align: left;">
        <div style="min-width: 1000px; border: 2px solid #98ff98; border-radius: 10px; padding: 15px; margin: 10px auto; max-width: 600px; background-color: rgba(240, 255, 240, 0.7);">
          <b style="font-size: 1.2em;">Conclusion 4:</b> <b style="font-size: 1.05em;">Language transfer ability remains critical for multilingual model performance in anesthesia reasoning. We recommend continued pre-training to address the deficiency in domain-specific knowledge across languages at the stable language ability stage.</b><br>
        </div>
      </figcaption>
    </figure>
  </div>

  <div style="flex: 0 1 45%; min-width: 1000px; margin-bottom: 40px;">
    <figure style="position: relative;">
      <img src="{{ site.baseurl }}/assets/models_length.png" alt="Model Scale Analysis" style="width: 100%;">
      <figcaption style="position: absolute; top: 110%; left: 50%; transform: translate(-50%, -50%); text-align: left;">
        <div style="min-width: 1000px; border: 2px solid #98ff98; border-radius: 10px; padding: 15px; margin: 10px auto; max-width: 600px; background-color: rgba(240, 255, 240, 0.7);">
          <b style="font-size: 1.2em;">Conclusion 5:</b> <b style="font-size: 1.05em;">Models that achieve superior performance on System2 questions often engage in longer CoT reasoning processes.</b><br>
        </div>
      </figcaption>
    </figure>
  </div>
</div>

# 😺 Impact of Training Strategies and Reasoning Techniques


<div style="width: 100%; display: flex; flex-wrap: wrap; justify-content: center; gap: 30px;">

  <div style="flex: 0 1 45%; margin-bottom: 30px; display: flex; justify-content: center; flex-direction: column;">
    <div style="display: flex; justify-content: center; width: 100%;">
    <table style="width: 100%; width: 600px; border-collapse: collapse;">
 <thead>
            <tr>
              <th style="text-align: center;" rowspan="2">Model</th>
              <th style="text-align: center;" colspan="2">SFT Data</th>
              <th style="text-align: center;" rowspan="2">Accuracy ANESBENCH</th>
            </tr>
            <tr>
              <th style="text-align: center;">AnesQA</th>
              <th style="text-align: center;">Medical-o1</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td style="text-align: center;">Qwen2.5-7B-Instruct</td>
              <td style="text-align: center;">-</td>
              <td style="text-align: center;">-</td>
              <td style="text-align: center;">51.5</td>
            </tr>
            <tr>
              <td style="text-align: center;" rowspan="3">Qwen2.5-7B-Base</td>
              <td style="text-align: center;">✓</td>
              <td style="text-align: center;">X</td>
              <td style="text-align: center;">49.3</td>
            </tr>
            <tr>
              <td style="text-align: center;">X</td>
              <td style="text-align: center;">✓</td>
              <td style="text-align: center;">49.1</td>
            </tr>
            <tr>
              <td style="text-align: center;">✓</td>
              <td style="text-align: center;">✓</td>
              <td style="text-align: center;">49.7</td>
            </tr>
            <tr>
              <td style="text-align: center;" rowspan="3">Qwen2.5-7B-Base-CPT</td>
              <td style="text-align: center;">✓</td>
              <td style="text-align: center;">X</td>
              <td style="text-align: center;">49.7</td>
            </tr>
            <tr>
              <td style="text-align: center;">X</td>
              <td style="text-align: center;">✓</td>
              <td style="text-align: center;">50.7</td>
            </tr>
            <tr>
              <td style="text-align: center;">✓</td>
              <td style="text-align: center;">✓</td>
              <td style="text-align: center;">51.2</td>
            </tr>
          </tbody>
    </table>
    </div>
    <figcaption style="position: relative; margin-top: 30px; text-align: left;">
      <div style="min-width: 1000px; border: 2px solid #98ff98; border-radius: 10px; padding: 15px; margin: 10px auto; max-width: 600px; background-color: rgba(240, 255, 240, 0.7);">
        <b style="font-size: 1.2em;">Conclusion x:</b> <b style="font-size: 1.05em;">test content</b><br>
      </div>
    </figcaption>
  </div>

  <div style="flex: 0 1 45%; margin-bottom: 30px; display: flex; justify-content: center; flex-direction: column;">
    <div style="display: flex; justify-content: center; width: 100%;">
    <table style="width: 100%; width: 600px; border-collapse: collapse;">
      <thead>
            <tr>
              <th style="text-align: center;">Reasoning Strategy</th>
              <th style="text-align: center;">Tree Width</th>
              <th style="text-align: center;">Beam Size</th>
              <th style="text-align: center;">Step Tokens</th>
              <th style="text-align: center;">Accuracy(%)</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td style="text-align: center;">None</td>
              <td style="text-align: center;">-</td>
              <td style="text-align: center;">-</td>
              <td style="text-align: center;">-</td>
              <td style="text-align: center;">51.2</td>
            </tr>
            <tr>
              <td style="text-align: center;" rowspan="2">Best-of-N [21]</td>
              <td style="text-align: center;">4</td>
              <td style="text-align: center;">-</td>
              <td style="text-align: center;">-</td>
              <td style="text-align: center;">51.5</td>
            </tr>
            <tr>
              <td style="text-align: center;">8</td>
              <td style="text-align: center;">-</td>
              <td style="text-align: center;">-</td>
              <td style="text-align: center;">51.5</td>
            </tr>
            <tr>
              <td style="text-align: center;" rowspan="2">Beam Search [19]</td>
              <td style="text-align: center;">4</td>
              <td style="text-align: center;">4</td>
              <td style="text-align: center;">32</td>
              <td style="text-align: center;">52.1</td>
            </tr>
            <tr>
              <td style="text-align: center;">8</td>
              <td style="text-align: center;">8</td>
              <td style="text-align: center;">32</td>
              <td style="text-align: center;"><strong>52.4</strong></td>
            </tr>
          </tbody>
    </table>
    </div>
    <figcaption style="position: relative; margin-top: 30px; text-align: left;">
      <div style="min-width: 1000px; border: 2px solid #98ff98; border-radius: 10px; padding: 15px; margin: 10px auto; max-width: 600px; background-color: rgba(240, 255, 240, 0.7);">
        <b style="font-size: 1.2em;">Conclusion x:</b> <b style="font-size: 1.05em;">test content</b><br>
      </div>
    </figcaption>
  </div>

  <div style="flex: 0 1 45%; min-width: 500px; margin-bottom: 30px;">
    <figure style="position: relative;">
      <img src="{{ site.baseurl }}/assets/impact_of_r1_distillation.png" alt="Model Scale Analysis" style="width: 100%;">
      <figcaption style="position: absolute; top: 110%; left: 50%; transform: translate(-50%, -50%); text-align: left;">
        <div style="min-width: 1000px; border: 2px solid #98ff98; border-radius: 10px; padding: 15px; margin: 10px auto; max-width: 600px; background-color: rgba(240, 255, 240, 0.7);">
        <b style="font-size: 1.2em;">Conclusion x:</b> <b style="font-size: 1.05em;">test content</b><br>
        </div>
      </figcaption>
    </figure>
  </div>
</div> -->
# Prompts

| File | Model | Used for | Placeholders |
|---|---|---|---|
| [`segmentation_prompt.txt`](segmentation_prompt.txt) | LLaMA-2 70B | Splitting a timestamped transcript into segments (segs) and sub-segments (subsegs) | `{transcript}` |
| [`query_generation_prompt.txt`](query_generation_prompt.txt) | GPT-3.5 Turbo | Generating natural, search-style queries from a transcript | `{video_id}`, `{transcript}` |

## Terminology

The segmentation prompt uses the words **subprocess** and **sub-subprocess**. They correspond to **segment (seg)** and **sub-segment (subseg)** in the paper.

## Notes

- `query_generation_prompt.txt` is written as a Python `str.format` template, so the literal braces of the JSON output format are escaped as `{{` and `}}`. Fill it with:

  ```python
  prompt = open("prompts/query_generation_prompt.txt").read().format(video_id=vid, transcript=text)
  ```

- `segmentation_prompt.txt` uses the LLaMA-2 chat format (`[INST]`, `<<SYS>>`). Replace `{transcript}` with the timestamped transcript of one video.
- Images of both prompts, as they appeared in the submitted paper, are in [`../figures/`](../figures/).

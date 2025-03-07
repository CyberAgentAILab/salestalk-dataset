# User Willingness-aware Sales Talk Dataset

This repository contains data for our paper ["User Willingness-aware Sales Talk Dataset"](https://aclanthology.org/2025.coling-main.742/) (COLING2025).

## Overview

The User Willingness-aware Sales Talk Dataset is a novel dataset designed to facilitate research on sales dialogue systems that explicitly consider user willingness. 
To ensure high ecological validity, we simulated real-world sales dialogue scenarios where participants interacted naturally. The dataset captures three crucial aspects of user willingness: (1) willingness to engage in a dialogue, (2) willingness to provide information, and (3) willingness to accept the salesperson's objective. The data was collected through a Wizard-of-Oz experiment, in which human users interacted with salespeople in a simulated environment.

The dataset consists of **109 dialogues** with a total of **3,289 utterances**. Each dialogue was evaluated at both the dialogue level and the utterance level to capture user willingness dynamically throughout the conversation. This fine-grained annotation allows researchers to analyze how user willingness evolves and affects the success of sales dialogues.


## Languages

All utterances in the dataset are in Japanese.

## Dataset Structure

This dataset is in JSON Lines format, where each line is a JSON object representing a dialogue. This dataset includes dialogue data such as the following:

### Example
```json
{
    "dialogue_id": 0,
    "sales_id": "SALES_0",
    "user_id": "USER_0",
    "user_dialogue_evals": [
        {
            "label": "before_purchase_intention",
            "raw_question": "掲載されている商品（ワイヤレスイヤホン）について、現時点で購入したいと思っていますか？",
            "raw_answer": "少しそう思う",
            "answer": 5
        },
        {
            "label": "after_purchase_intention",
            "raw_question": "掲載されている商品（ワイヤレスイヤホン）について、現時点で購入したいと思っていますか？",
            "raw_answer": "少しそう思う",
            "answer": 5
        }
    ],
    "utterances": [
        {
            "utterance_id": "0_0",
            "timestamp": "2024-02-22T10:30:49",
            "speaker": "system",
            "message": "*注意事項*\n- 右側に商品が表示されないなど、画面が正常に表示されない場合はページをリロードしてください。\n- Google翻訳などの自動翻訳機能はオフにしてください。\n- その他問題が発生した場合は、実験責任者に問い合わせてください。\n- ユーザ役は、お好きなタイミングで対話終了もしくは商品を購入していただいて構いません。\n- 対話実験は、必ず対話終了ボタンもしくは商品購入ボタンを押して終了させてください。\n- 対話時間は、30分を超えないようにしてください。\n- このあと、セールスBotからメッセージが送信されます。メッセージが送信されるまでしばらくお待ちください。\n        ",
            "user_utterance_evals": []
        },
        {
            "utterance_id": "0_1",
            "timestamp": "2024-02-22T10:31:12",
            "speaker": "sales",
            "message": "こんにちは！本日はどのような商品をお探しですか？",
            "user_utterance_evals": [
                {
                    "label": "CONTINUING_DIALOGUE",
                    "raw_question": "この発話は**少しでも**会話を続けたい気持ちに影響を与えましたか？",
                    "raw_answer": "ポジティブな影響を与えた",
                    "answer": "positive"
                },
                {
                    "label": "PROVIDING_INFORMATION",
                    "raw_question": "この発話は**少しでも**情報を提供したい気持ちに影響を与えましたか？",
                    "raw_answer": "ポジティブな影響を与えた",
                    "answer": "positive"
                },
                {
                    "label": "GOAL_ACCEPTANCE",
                    "raw_question": "この発話は**少しでも**商品を買いたい気持ちに影響を与えましたか？",
                    "raw_answer": "ポジティブな影響を与えた",
                    "answer": "positive"
                }
            ]
        },
        {
            "utterance_id": "0_2",
            "timestamp": "2024-02-22T10:32:06",
            "speaker": "user",
            "message": "ワイヤレスイヤホン",
            "user_utterance_evals": []
        },
        {
            "utterance_id": "0_3",
            "timestamp": "2024-02-22T10:32:28",
            "speaker": "sales",
            "message": "承知しました！",
            "user_utterance_evals": [
                {
                    "label": "CONTINUING_DIALOGUE",
                    "raw_question": "この発話は**少しでも**会話を続けたい気持ちに影響を与えましたか？",
                    "raw_answer": "全く影響がなかった",
                    "answer": "neutral"
                },
                {
                    "label": "PROVIDING_INFORMATION",
                    "raw_question": "この発話は**少しでも**情報を提供したい気持ちに影響を与えましたか？",
                    "raw_answer": "全く影響がなかった",
                    "answer": "neutral"
                },
                {
                    "label": "GOAL_ACCEPTANCE",
                    "raw_question": "この発話は**少しでも**商品を買いたい気持ちに影響を与えましたか？",
                    "raw_answer": "全く影響がなかった",
                    "answer": "neutral"
                }
            ]
        },
       [...]
    ]
}
```


## Citation

If you use our dataset, please cite our paper:

```bibtex
@inproceedings{hentona-etal-2025-user,
    title = "User Willingness-aware Sales Talk Dataset",
    author = "Hentona, Asahi  and
      Baba, Jun  and
      Sato, Shiki  and
      Akama, Reina",
    booktitle = "Proceedings of the 31st International Conference on Computational Linguistics",
    month = jan,
    year = "2025",
    address = "Abu Dhabi, UAE",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2025.coling-main.742/",
    pages = "11206--11217",
}
```

## License
<p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/">
<span property="dct:title">User Willingness-aware Sales Talk Dataset</span>  by CyberAgent AI Lab is licensed under <a href="https://creativecommons.org/licenses/by-nc-sa/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">CC BY-NC-SA 4.0<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/nc.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/sa.svg?ref=chooser-v1" alt=""></a></p>
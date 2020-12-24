当前的数据总共包含以下几份文件：
|- train_base.json 是原始训练集，包含质押、股份股权转让、投资、起诉和减持五个类别
|- train_trans.json 是迁移训练集，包含收购和判决这两个类别
|- dev_base.json 是原始验证集，包含质押、股份股权转让、投资、起诉和减持五个类别
|- dev_trans.json 是迁移验证集，包含收购和判决这两个类别

注意：
根据 train_base.json 和 train_trans.json 做模型训练，然后在 dev_base.json 和 dev_trans.json 做模型推断。


train
{
    "id": "4c02ce54ad9c63762ffe6b6add858ddb",
    "content": "此前,携程曾发公告称百度抛售持股1/3,这是百度在第三季度产生的最大股权投资变动,而携程整体市值起伏不定或是百度投资收益受损的主要原因。",
    "events": [
        {
            "type": "股份股权转让",
            "mentions": [
                {
                    "word": "抛售",
                    "span": [
                        12,
                        14
                    ],
                    "role": "trigger"
                },
                {
                    "word": "百度",
                    "span": [
                        10,
                        12
                    ],
                    "role": "sub-org"
                },
                {
                    "word": "股权",
                    "span": [
                        34,
                        36
                    ],
                    "role": "collateral"
                },
                {
                    "word": "携程",
                    "span": [
                        3,
                        5
                    ],
                    "role": "target-company"
                }
            ]
        }
    ]
}


dev
{
    "id": "d45bb6fb70598b9a472c14d28ad12708",
    "content": "上述股权已于2012年9月25日办理了股权质押登记手续,股权质押期限自股权质押登记之日起至质权人办理解除质押登记为止。"
}
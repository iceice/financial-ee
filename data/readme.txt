当前的数据总共包含以下几份文件：
|- train_base.json 是原始训练集，包含质押、股份股权转让、投资、起诉和减持五个类别
|- train_trans.json 是迁移训练集，包含收购和判决这两个类别
|- dev_base.json 是原始验证集，包含质押、股份股权转让、投资、起诉和减持五个类别
|- dev_trans.json 是迁移验证集，包含收购和判决这两个类别

注意：
根据 train_base.json 和 train_trans.json 做模型训练，然后在 dev_base.json 和 dev_trans.json 做模型推断。
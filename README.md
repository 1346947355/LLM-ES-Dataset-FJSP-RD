LLM-ES Dataset: FJSP-RD

This repository provides the dataset developed for LLM-ES research. LLM-ES is a sequential decision-making paradigm for Flexible Job Shop Scheduling (FJSP).
This dataset is intended to facilitate academic communication, research, and reproducibility in related research fields.
Current Status: This dataset is currently released for academic research and non-commercial purposes. Please carefully review the following license and usage terms before using or redistributing the dataset.
________________________________________
1. Dataset
1.1 Sample Data

| A simplified sample |
| :--- |
| Instruction: <br>This flexible job shop scheduling problem has 3 jobs and 3 machines.  Generate a near-optimal schedule.  |
| System: <br>The makespan is the completion time of the last operation in the schedule.  Each job J has a precedence constraint between its operations O,for example, operation O1_2 must be assigned before O1_3.  Each machine M can process only one operation O of one job J at a time, and once an operation starts, it cannot be interrupted… |
| Input:<br>
{"n_jobs": 3, "n_machines": 3, "machines": ["M1", "M2", "M3"], "jobs": [
<br>{"job_id": "job1", "operations": [{"op_id": "O1_1", "opt_machine_times": {"M1": 8, "M2": 6, "M3": 3}}, {"op_id": "O1_2", "opt_machine_times": {"M2": 9}}]}, 
<br>{"job_id": "job2", "operations": [{"op_id": "O2_1", "opt_machine_times": {"M1": 5, "M2": 6}}, {"op_id": "O2_2", "opt_machine_times": {"M1": 10}}]}, 
<br>{"job_id": "job3", "operations": [{"op_id": "O3_1", "opt_machine_times": {"M1": 3}}, {"op_id": "O3_2", "opt_machine_times": {"M2": 5, "M3": 9}}]}]} |
| Output:<br>
{"assignments": {"O1_1": "M3", "O1_2": "M2", "O2_1": "M2", "O2_2": "M1", "O3_1": "M1", "O3_2": "M2"}, "sequence": ["O1_1", "O2_1", "O3_1", "O1_2", "O3_2", "O2_2"], "schedule": [
<br>{"op_id": "O1_1", "machine": "M3", "start": 0, "finish": 3, "proc_time": 3},
<br>{"op_id": "O2_1", "machine": "M2", "start": 0, "finish": 6, "proc_time": 6},
<br>{"op_id": "O3_1", "machine": "M1", "start": 0, "finish": 3, "proc_time": 3},
<br>{"op_id": "O1_2", "machine": "M2", "start": 3, "finish": 12, "proc_time": 9},
<br>{"op_id": "O3_2", "machine": "M2", "start": 6, "finish": 11, "proc_time": 5},
<br>{"op_id": "O2_2", "machine": "M1", "start": 12, "finish": 22, "proc_time": 10}],  ….. 
<br>"makespan": 22} |

________________________________________
1.2 Dataset Statistics
Item	Information
Dataset Name	FJSP-RD
Data Type	JSON
Data Organization	JSON Array
Number of Samples	30,000
Dataset Size	2.65 GB
Task Type	Flexible Job Shop Scheduling
Intended Use	Supervised Fine-Tuning
Language	English
________________________________________
2. Directory Structure
LLM-ES-FJSP/
│
├── README.md
│
├── dataset/
│   └── ...
│
└── training/
    └── ...

The dataset/ directory is used to store dataset-related files or provide information on how to obtain the complete dataset.
The training/ directory is used to store publicly available model training resources related to this project.
Complete Dataset: 【To be determined】
________________________________________
3. Usage

This dataset is primarily intended for academic research, education, and other non-commercial purposes.
Subject to the terms of this license and applicable laws and regulations, users may copy, redistribute, analyze, modify, and otherwise use the dataset for non-commercial research purposes.

Users are required to:

Provide appropriate attribution and citation for this dataset and the associated research;
Provide a link to the CC BY-NC 4.0 license under which this dataset is released;
Clearly indicate any modifications made to the dataset;
Comply with applicable laws, regulations, and other relevant intellectual property requirements;
Not use the dataset for commercial purposes;
Not imply, in any manner, that the authors endorse, sponsor, or officially support the user, the user's research results, or any related products.

If you use this dataset in a paper, report, software project, or other academic research, please cite the relevant research according to Section 6.
________________________________________
4. Rights and License
4.1 CC BY-NC 4.0

This dataset is released under the Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0) license.

License:
CC BY-NC 4.0 International
Subject to the terms of the CC BY-NC 4.0 license, users may:
Copy and redistribute the dataset;
Modify, adapt, transform, or further process the dataset;
Use the dataset for academic research, education, and other non-commercial purposes.

Users must:
Provide appropriate attribution to the original dataset author;
Provide a link to the CC BY-NC 4.0 license;
Indicate any modifications made to the dataset;
Not use the dataset for commercial purposes;
Not imply that the author endorses the user or the user's use of the dataset.
Under CC BY-NC 4.0, NonCommercial means that the use is not primarily intended for or directed toward commercial advantage or monetary compensation. The specific definition and complete license terms are governed by the official Creative Commons license text.
Full License:
Creative Commons Attribution-NonCommercial 4.0 International
________________________________________
4.2 Dataset Rights

Author: wen
As the author and dataset builder, I hold the applicable rights to the original data content independently created for this dataset and make such content available to the public under the CC BY-NC 4.0 license within the scope described in this README.
The public release of this repository does not constitute a transfer of ownership or other intellectual property rights in the dataset.
Except for the rights expressly granted under CC BY-NC 4.0, all other rights remain with the respective rights holders.
________________________________________
4.3 Third-Party Materials

If the dataset contains any third-party data, software, benchmark instances, text, model outputs, or other content subject to third-party rights, such content may not be covered by the CC BY-NC 4.0 license.
For third-party materials, users must comply with the original license terms, terms of use, and applicable intellectual property requirements.
If any content in the dataset is subject to third-party rights or other legal restrictions, those third-party rights and restrictions shall apply to the relevant content.
________________________________________
5. Patent Notice

This dataset is released under the CC BY-NC 4.0 license.
CC BY-NC 4.0 does not grant any express or implied patent license. The public release of this repository should not be interpreted as granting users any right to practice, make, use, sell, offer for sale, import, or otherwise exploit any invention that may be protected by patent rights.
Users are solely responsible for determining whether their use of the dataset, related methods, software, or derivative results is subject to any patent or other intellectual property restrictions.
If the research results, methods, or technologies associated with this dataset are subject to pending or granted patent rights, the public release of this dataset does not affect the validity of such patent rights.
For provisions concerning patent rights under CC BY-NC 4.0, please refer to the official Creative Commons license text.
________________________________________
6. Citation

If you use this dataset in academic research, please cite the associated paper:
【Citation to be added】
________________________________________
7. Disclaimer

This dataset is provided "AS IS". To the maximum extent permitted by applicable law, the authors make no express or implied warranties regarding the dataset.
The authors do not warrant that the dataset:
Is complete or free of errors;
Will always be available;
Is suitable for any particular research purpose;
Will meet any specific requirements of users;
Will guarantee any particular experimental results or research conclusions.
To the extent permitted by applicable law, the authors shall not be liable for any direct, indirect, incidental, special, consequential, or other damages arising from the use of this dataset or any related materials provided through this repository.
Users are solely responsible for determining whether the dataset is suitable for their intended use and for complying with applicable laws, license terms, and intellectual property requirements.
________________________________________
8. Contact
If you have any questions regarding this dataset, the license, or usage permissions, please submit an Issue through this repository or contact the corresponding author of the associated paper.
________________________________________
9. Acknowledgment
This dataset is intended for research related to large language models and Flexible Job Shop Scheduling.
We acknowledge the developers and maintainers of the public benchmark data, open-source software, libraries, and related tools used in this research.
________________________________________
License

CC BY-NC 4.0
Copyright © 2026 wen zhimin
This dataset is licensed under the Creative Commons Attribution-NonCommercial 4.0 International License.
________________________________________________________________________________________________________________________

LLM-ES 数据集：FJSP-RD
本仓库提供用于 LLM-ES 研究的数据集。LLM-ES 是一种面向柔性作业车间调度（FJSP）的顺序决策范式。
本数据集旨在促进相关研究领域的学术交流、科研使用与研究复现。
当前状态： 本数据集目前面向学术研究及非商业用途开放。在使用或再分发本数据集之前，请仔细阅读以下许可与使用条款。
________________________________________
1. 数据集
1.1 数据集样本示例
| 一个简化样本示例 |
| :--- |
| Instruction: <br>This flexible job shop scheduling problem has 3 jobs and 3 machines.  Generate a near-optimal schedule.  |
| System: <br>The makespan is the completion time of the last operation in the schedule.  Each job J has a precedence constraint between its operations O,for example, operation O1_2 must be assigned before O1_3.  Each machine M can process only one operation O of one job J at a time, and once an operation starts, it cannot be interrupted… |
| Input:<br>
{"n_jobs": 3, "n_machines": 3, "machines": ["M1", "M2", "M3"], "jobs": [
<br>{"job_id": "job1", "operations": [{"op_id": "O1_1", "opt_machine_times": {"M1": 8, "M2": 6, "M3": 3}}, {"op_id": "O1_2", "opt_machine_times": {"M2": 9}}]}, 
<br>{"job_id": "job2", "operations": [{"op_id": "O2_1", "opt_machine_times": {"M1": 5, "M2": 6}}, {"op_id": "O2_2", "opt_machine_times": {"M1": 10}}]}, 
<br>{"job_id": "job3", "operations": [{"op_id": "O3_1", "opt_machine_times": {"M1": 3}}, {"op_id": "O3_2", "opt_machine_times": {"M2": 5, "M3": 9}}]}]} |
| Output:<br>
{"assignments": {"O1_1": "M3", "O1_2": "M2", "O2_1": "M2", "O2_2": "M1", "O3_1": "M1", "O3_2": "M2"}, "sequence": ["O1_1", "O2_1", "O3_1", "O1_2", "O3_2", "O2_2"], "schedule": [
<br>{"op_id": "O1_1", "machine": "M3", "start": 0, "finish": 3, "proc_time": 3},
<br>{"op_id": "O2_1", "machine": "M2", "start": 0, "finish": 6, "proc_time": 6},
<br>{"op_id": "O3_1", "machine": "M1", "start": 0, "finish": 3, "proc_time": 3},
<br>{"op_id": "O1_2", "machine": "M2", "start": 3, "finish": 12, "proc_time": 9},
<br>{"op_id": "O3_2", "machine": "M2", "start": 6, "finish": 11, "proc_time": 5},
<br>{"op_id": "O2_2", "machine": "M1", "start": 12, "finish": 22, "proc_time": 10}],  ….. 
<br>"makespan": 22} |

========================================================
1.2 数据集统计信息
| 项目 | 信息 |
| :--- | :--- |
| 数据集名称 | FJSP-RD |
| 数据类型 | JSON |
| 数据组织形式 | JSON Array |
| 样本数量 | 30,000 |
| 数据集大小 | 2.65 GB |
| 任务类型 | Flexible Job Shop Scheduling |
| 数据用途 | Supervised Fine-Tuning |
| 语言 | English |
________________________________________
2. 目录结构
LLM-ES-FJSP/
│
├── README.md
│
├── dataset/
│   └── ...
│
└── training/
    └── ...
dataset/ 目录用于存放数据集相关文件或提供完整数据集的获取信息。
training/ 目录用于存放本项目公开的模型训练相关资源。
完整数据集： 【待定】
________________________________________
3. 使用说明
本数据集主要用于学术研究、教育以及其他非商业用途。
在遵守本许可协议及适用法律法规的前提下，使用者可以对本数据集进行复制、再分发、分析、修改和其他非商业研究用途的使用。
使用者应当：
•	对本数据集及相关研究进行适当署名和引用；
•	提供本数据集所采用的 CC BY-NC 4.0 许可协议链接；
•	在对本数据集进行修改时明确说明所作修改；
•	遵守适用的法律法规及其他相关知识产权要求；
•	不得将本数据集用于商业目的；
•	不得以任何方式暗示作者对使用者、使用者的研究成果或相关产品提供认可、赞助或官方支持。
如果您在论文、报告、软件或其他学术研究中使用本数据集，请按照 第 6 节 的说明引用相关研究。
________________________________________
4. 权利与许可声明
4.1 CC BY-NC 4.0
本数据集采用 Creative Commons Attribution-NonCommercial 4.0 International（CC BY-NC 4.0） 许可协议进行授权。
许可协议：
CC BY-NC 4.0 International
在遵守 CC BY-NC 4.0 许可协议条款的前提下，使用者可以：
•	复制和再分发本数据集；
•	对本数据集进行修改、调整、转换或进一步处理；
•	将本数据集用于学术研究、教育和其他非商业用途。
使用者必须：
•	对原始数据集作者进行适当署名；
•	提供 CC BY-NC 4.0 许可协议的链接；
•	在对数据集进行修改时说明所作修改；
•	不得将本数据集用于商业目的；
•	不得通过使用本数据集暗示作者对使用者或其使用方式提供认可或支持。
CC BY-NC 4.0 中的“非商业”使用，是指不主要以商业优势或金钱补偿为目的或导向的使用。具体定义及完整许可条件以 Creative Commons 官方许可文本为准。
完整许可协议：
https://creativecommons.org/licenses/by-nc/4.0/
________________________________________
4.2 数据集权利声明
【作者：wen zhimin】
作为本数据集的作者/数据集构建者，对本人原创生成的数据内容依法享有相应的权利，并在本 README 所述范围内按照 CC BY-NC 4.0 许可协议向公众提供使用权限。
本仓库的公开发布不构成对数据集所有权或其他知识产权的转让。
除 CC BY-NC 4.0 明确授予的权利外，其他权利仍由相应权利人保留。
________________________________________
4.3 第三方材料
如果本数据集包含任何第三方数据、软件、基准实例、文本、模型输出或其他受第三方权利约束的内容，则相关内容可能不属于本 CC BY-NC 4.0 许可范围。
对于第三方材料，使用者应遵守其原始许可协议、使用条款及适用的知识产权规定。
如本数据集中的任何内容受到第三方权利或其他法律限制，则相关第三方权利和限制优先适用。
________________________________________
5. 专利声明
本数据集采用 CC BY-NC 4.0 许可协议进行发布。
CC BY-NC 4.0 不构成任何明示或默示的专利许可。
本仓库的公开发布不应被理解为授予使用者实施、制造、使用、销售、许诺销售、进口或以其他方式实施任何可能受专利权保护的发明的权利。
使用者应自行判断其对本数据集、相关方法、软件或衍生成果的使用是否涉及任何专利权或其他知识产权限制，并自行承担相应责任。
如相关研究成果、方法或技术涉及已申请或已授权的专利权，本数据集的公开发布不影响相关专利权的效力。
有关 CC BY-NC 4.0 对专利权的规定，请以 Creative Commons 官方许可文本为准。
________________________________________
6. 引用方式
如果您在学术研究中使用本数据集，请引用相关论文：

________________________________________
7. 免责声明
本数据集按照 “AS IS” 提供。在适用法律允许的最大范围内，作者不对本数据集作出任何明示或默示的保证。
作者不保证本数据集：
•	完整且不存在错误；
•	始终可用；
•	适用于特定研究目的；
•	能够满足使用者的特定需求；
•	能够保证任何特定实验结果或研究结论。
在适用法律允许的范围内，对于因使用本数据集或本仓库所提供的相关材料而产生的任何直接、间接、偶然、特殊、后果性或其他损害，作者不承担责任。
使用者应自行判断本数据集是否适合其预期用途，并自行遵守适用的法律法规、许可协议以及知识产权要求。
________________________________________
8. 联系方式
如对本数据集、许可协议或使用权限存在疑问，请通过本仓库提交 Issue，或联系相关论文的通讯作者。

________________________________________
9. 致谢
本数据集用于大语言模型与柔性作业车间调度相关研究。
感谢本研究所使用的公开基准数据、开源软件、程序库及相关工具的开发者和维护者。
________________________________________
License
CC BY-NC 4.0
Copyright © 【2026】 【wen zhimin】
This dataset is licensed under the Creative Commons Attribution-NonCommercial 4.0 International License.
https://creativecommons.org/licenses/by-nc/4.0/


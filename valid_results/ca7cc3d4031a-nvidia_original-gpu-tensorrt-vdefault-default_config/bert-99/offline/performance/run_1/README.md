This experiment is generated using the [MLCommons Collective Mind automation framework (CM)](https://github.com/mlcommons/cm4mlops).

*Check [CM MLPerf docs](https://docs.mlcommons.org/inference) for more details.*

## Host platform

* OS version: Linux-5.15.0-126-generic-x86_64-with-glibc2.29
* CPU version: x86_64
* Python version: 3.8.10 (default, Nov  7 2024, 13:10:47) 
[GCC 9.4.0]
* MLCommons CM version: 3.5.1.1

## CM Run Command

See [CM installation guide](https://docs.mlcommons.org/inference/install/).

```bash
pip install -U cmind

cm rm cache -f

cm pull repo mlcommons@cm4mlops --checkout=5c26d813223a310a73dd844af98be626f66fc2f7

cm run script \
	--tags=run-mlperf,inference,_r4.1-dev,_all-scenarios \
	--model=bert-99 \
	--implementation=nvidia \
	--framework=tensorrt \
	--category=edge \
	--execution_mode=valid \
	--device=cuda
```
*Note that if you want to use the [latest automation recipes](https://docs.mlcommons.org/inference) for MLPerf (CM scripts),
 you should simply reload mlcommons@cm4mlops without checkout and clean CM cache as follows:*

```bash
cm rm repo mlcommons@cm4mlops
cm pull repo mlcommons@cm4mlops
cm rm cache -f

```
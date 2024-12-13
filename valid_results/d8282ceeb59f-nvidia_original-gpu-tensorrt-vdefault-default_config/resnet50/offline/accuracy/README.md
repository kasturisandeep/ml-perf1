This experiment is generated using the [MLCommons Collective Mind automation framework (CM)](https://github.com/mlcommons/cm4mlops).

*Check [CM MLPerf docs](https://docs.mlcommons.org/inference) for more details.*

## Host platform

* OS version: Linux-5.4.0-167-generic-x86_64-with-glibc2.29
* CPU version: x86_64
* Python version: 3.8.10 (default, Nov  7 2024, 13:10:47) 
[GCC 9.4.0]
* MLCommons CM version: 3.5.1.1

## CM Run Command

See [CM installation guide](https://docs.mlcommons.org/inference/install/).

```bash
pip install -U cmind

cm rm cache -f

cm pull repo mlcommons@mlperf-automations --checkout=f5e04069c8d7395be34f94fa8a94edc6c317b58e

cm run script \
	--tags=run-mlperf,inference,_r4.1-dev,_all-scenarios \
	--model=resnet50 \
	--implementation=nvidia \
	--framework=tensorrt \
	--category=edge \
	--execution_mode=valid \
	--device=cuda
```
*Note that if you want to use the [latest automation recipes](https://docs.mlcommons.org/inference) for MLPerf (CM scripts),
 you should simply reload mlcommons@mlperf-automations without checkout and clean CM cache as follows:*

```bash
cm rm repo mlcommons@mlperf-automations
cm pull repo mlcommons@mlperf-automations
cm rm cache -f

```
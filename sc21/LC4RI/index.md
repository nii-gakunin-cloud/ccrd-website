---
title: Reproducibility Extensions for Jupyter Notebook (LC4RI tools)
layout: default
redirect_to: "https://literate-computing.github.io/fastpages/tools_en/"
---

Literate Computing Tools are our enhancements to Jupyter for achieving the following goals:
- Giving awareness where you are; the cells are colored depending on their statuses. You can see how an operation is in progress and whether it has been succeeded. Light Cyan, Linen, and Pink represent “running”, “finished successfully” and “finished with errors” respectively.
- Preventing miss-operation; once a cell has been executed, it “freezes” against unintended execution. Frozen cells will not be executed nor edited until those will be unfrozen.
- A good operational outlook; as an enhancement for collapsible headings, collapsed code cells underneath are represented as bricks. The number of bricks represents operational complexities. Plus, you can run through whole bricks (collapsed code cells) with one click as a routine procedure. Color changes of bricks also represent the progress.
- Assure traceability; infrastructure operation can generate massive output lines. LC_wrapper kernel summarizes output lines, and simultaneously all original output lines are saved into an individual file with a timestamp at each execution. You can investigate the total output and compare it with previous results for reviewing.


# Try the Demo

A Docker Image containing all our tools is available in the [Jupyter-LC_docker](https://github.com/NII-cloud-operation/Jupyter-LC_docker) repository.
You can start the Notebook server on port 8888 with the following command.

```
docker run -it --rm -p 8888:8888 niicloudoperation/notebook:latest
```

<iframe src="https://ghbtns.com/github-btn.html?user=NII-cloud-operation&repo=Jupyter-LC_docker&type=star&count=true" frameborder="0" scrolling="0" width="150" height="20" title="GitHub"></iframe>

You can login the Notebook server with the authentication token in the startup message.

## Jupyter Extensions

### [LC_run_through Extension](https://github.com/NII-cloud-operation/Jupyter-LC_run_through)

<iframe src="https://ghbtns.com/github-btn.html?user=NII-cloud-operation&repo=Jupyter-LC_run_through&type=star&count=true" frameborder="0" scrolling="0" width="150" height="20" title="GitHub"></iframe>

{% include youtube.html content='pkzE_nwtEKQ' %}

### [LC_wrapper Kernel](https://github.com/NII-cloud-operation/Jupyter-LC_wrapper)

<iframe src="https://ghbtns.com/github-btn.html?user=NII-cloud-operation&repo=Jupyter-LC_wrapper&type=star&count=true" frameborder="0" scrolling="0" width="150" height="20" title="GitHub"></iframe>

{% include youtube.html content='-28XG7aHYY8' %}

### Other Extensions

- [multi_outputs](https://github.com/NII-cloud-operation/Jupyter-multi_outputs)
- [nblineage](https://github.com/NII-cloud-operation/Jupyter-LC_nblineage)
- [Jupyter-LC_index](https://github.com/NII-cloud-operation/Jupyter-LC_index)
- [sidestickies](https://github.com/NII-cloud-operation/sidestickies)
- [nbsearch](https://github.com/NII-cloud-operation/nbsearch)

## Platforms for Reproducible Infrastructure

- [OperationHub](https://github.com/NII-cloud-operation/OperationHub)

## Notebooks for Reproducible Infrastructure

- [Literate-computing-Basics](https://github.com/NII-cloud-operation/Literate-computing-Basics)
- [Literate-computing-Hadoop](https://github.com/NII-cloud-operation/Literate-computing-Hadoop)
- [Literate-computing-Elasticsearch](https://github.com/NII-cloud-operation/Literate-computing-Elasticsearch)

---
title: "View the Formula for a Time Series Model (Data Mining) | Microsoft Docs"
ms.custom: ""
ms.date: "03/02/2016"
ms.prod: "analysis-services"
ms.prod_service: "analysis-services"
ms.service: ""
ms.component: ""
ms.reviewer: ""
ms.suite: "pro-bi"
ms.technology: 
  - "analysis-services"
  - "analysis-services/data-mining"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "data mining [Analysis Services], how-to topics"
  - "ARTXP"
  - "time series algorithms [Analysis Services]"
  - "ARIMA"
  - "time series [Analysis Services]"
  - "Time Series Viewer [Analysis Services]"
ms.assetid: 825ef719-2f44-4979-be01-5a81f54e1a53
caps.latest.revision: 14
author: "Minewiskan"
ms.author: "owend"
manager: "kfile"
ms.workload: "Inactive"
---
# View the Formula for a Time Series Model (Data Mining)
[!INCLUDE[ssas-appliesto-sqlas](../../includes/ssas-appliesto-sqlas.md)]
  If you created a time series model using [!INCLUDE[ssNoVersion](../../includes/ssnoversion-md.md)] Data Mining, the easiest way to see the regression equation for the model is to use the **Mining Legend** of the [Microsoft Time Series Viewer](../../analysis-services/data-mining/browse-a-model-using-the-microsoft-time-series-viewer.md), which presents all the constants in a readable format.  
  
### To view the ARTXP regression formula for a time series model  
  
1.  In [!INCLUDE[ssManStudioFull](../../includes/ssmanstudiofull-md.md)], select the time series model that you want to view, and click **Browse**.  
  
     -- or --  
  
     In [!INCLUDE[ssBIDevStudioFull](../../includes/ssbidevstudiofull-md.md)], select the time series model, and then click the **Mining Model Viewer** tab.  
  
2.  Click the **Model** tab.  
  
3.  If the model contains multiple trees, select a single tree from the **Tree** drop-down list.  
  
    > [!NOTE]  
    >  A model will always have multiple trees if you have more than one data series. However, you will not see as many trees in the **Time Series viewer** as you will see in the [Microsoft Generic Content Tree Viewer](http://msdn.microsoft.com/library/751b4393-f6fd-48c1-bcef-bdca589ce34c). That is because the Time Series viewer combines the ARIMA and ARTXP information for each data series into a single representation.  
  
4.  Click any leaf node in the tree.  
  
     Nodes that are labeled as **Data Series** are always leaf nodes and can contain an equation. If an **(All)** node has no child nodes, it can also contain an equation.  
  
5.  If the **Mining Legend** is not available, right-click the node, and select **Show Legend**.  
  
     The ARTXP formula is displayed in the first half of the **Mining Legend**, as the **Tree node equation**.  
  
     ![viewing the time series formula in the legend](../../analysis-services/data-mining/media/ssdm-timeserieslegend.png "viewing the time series formula in the legend")  
  
### To view the ARIMA formula for a time series model  
  
1.  In [!INCLUDE[ssManStudioFull](../../includes/ssmanstudiofull-md.md)], select the time series model that you want to view, and click **Browse**.  
  
     -- or --  
  
     In [!INCLUDE[ssBIDevStudioFull](../../includes/ssbidevstudiofull-md.md)], select the time series model, and then click the **Mining Model Viewer** tab.  
  
2.  Click the **Model** tab.  
  
3.  If the model contains multiple trees, select a single tree from the **Tree** drop-down list.  
  
    > [!NOTE]  
    >  The model will always have multiple trees if you include more than one data series.  
  
4.  Click any node in the tree.  
  
     The ARIMA formula is displayed in the second half of the **Mining Legend**, as the **ARIMA equation**.  
  
5.  If the **Mining Legend** is not available, right-click the node, and select **Show Legend**.  
  
### To get the coefficients and terms for the equation  
  
1.  You can also get the terms and coefficients of the regression formula for a time series model by creating a **content query** on the model content.  
  
     For more information, see [Time Series Model Query Examples](../../analysis-services/data-mining/time-series-model-query-examples.md)  
  
2.  You can also browse the time series models and find the terms and coefficients by using the [Microsoft Generic Content Tree Viewer](http://msdn.microsoft.com/library/751b4393-f6fd-48c1-bcef-bdca589ce34c).  
  
     For more information, see [Mining Model Content for Time Series Models &#40;Analysis Services - Data Mining&#41;](../../analysis-services/data-mining/mining-model-content-for-time-series-models-analysis-services-data-mining.md).  
  
    > [!NOTE]  
    >  If you browse the content of a mixed model that uses both the ARIMA and ARTXP models, the two models are in separate trees, joined at the root node representing the model. Even though the ARIMA and ARTXP models are presented in one viewer for convenience, the structures are very different, as are the equations, which cannot be combined or compared. The ARTXP tree is more like a decision tree, whereas the ARIMA tree represents a series of moving averages.  
  
## See Also  
 [Mining Model Viewer Tasks and How-tos](../../analysis-services/data-mining/mining-model-viewer-tasks-and-how-tos.md)   
 [Browse a Model Using the Microsoft Time Series Viewer](../../analysis-services/data-mining/browse-a-model-using-the-microsoft-time-series-viewer.md)  
  
  

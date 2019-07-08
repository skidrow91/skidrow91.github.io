---
layout: post
title: How to get product attribute value in magento 2
description: "How to get product attribute value in magento 2"
categories: magento
---

To get attribute value of product with store_id is 0, we can:

~~~~

    public function __construct(\Magento\Catalog\Api\ProductRepositoryInterface $productRepository) {
        $this->productRepository = $productRepository;
    }

    public function execute(){
        $productId = xxx;
        $product = $this->productRepository->getById($productId, false, 0);
        echo $product->getData('attribute-code');
    }

~~~~
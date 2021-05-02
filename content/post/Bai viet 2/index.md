---
title: Phân cụm văn bản bằng Non-negative Matrix Factorization
subtitle: Bài viết này chúng ta cùng tìm hiểu về NMF và ứng dụng cho bài toán phân cụm văn bản.

# Summary for listings and search engines
summary: Bài viết này chúng ta cùng tìm hiểu về NMF và ứng dụng cho bài toán phân cụm văn bản.

# Link this post with a project
projects: []

# Date published
date: "2021-04-30T00:00:00Z"

# Date updated
lastmod: "2020-12-13T00:00:00Z"

# Is this an unpublished draft?
draft: false

# Show this page in the Featured widget?
featured: false

# Featured image
# Place an image named `featured.jpg/png` in this page's folder and customize its options here.
image:
  caption: 'Image credit: [**Unsplash**](https://unsplash.com/photos/CpkOjOcXdUY)'
  focal_point: ""
  placement: 2
  preview_only: false

authors:
- admin

tags:
- Academic
- Data ming

categories:
- Demo
- NMF
---

## Phân cụm văn bản bằng Non-negative Matrix Factorization

Trong bài viết này chúng ta cùng tìm hiểu về NMF và ứng dụng cho bài toán phân cụm văn bản. 
Trước hết ta xét bài toán phân cụm văn bản như sau: 

Cho một dataset **D** trong đó có **n** văn bản. Sau khi tiền xử lý ta có ma trận **X** gồm **n** dòng và **m** cột, **m** cột này tương ứng với tập tất cả các từ xuất hiện trong dataset. Lưu ý để có được ma trận này dataset thường đã qua bước tiền xử lý bao gồm chuyển câu thành từ, loại bỏ các dấu, các từ không quan trọng, vv ... Bạn có thể tìm hiểu thêm về tiền xử lý dữ liệu văn bản [tại đây](https://towardsdatascience.com/machine-learning-text-processing-1d5a2d638958), hoặc [tại đây](https://www.kdnuggets.com/2017/12/general-approach-preprocessing-text-data.html).

Lưu ý khác là với dữ liệu văn bản, thường sẽ thưa (có nhiều giá trị 0) và có số chiều rất lớn, do đó trực tiếp áp dụng giải thuật phân cụm như K-means có thể sẽ không hiệu quả. Vì vậy, ta cùng tìm hiểu giải thuật hiệu quả hơn, đó là giải quyết bài toán phân cụm bằng NMF, ta cùng tìm hiểu kỹ thuật NMF nhé. 

### Non-negative matrix factorization (NMF)
Một cách ngắn gọn, có thể hiểu NMF là một kỹ thuật giảm số chiều (dimensionality reduction) của dữ liệu mà không làm mất các đặc trưng chính của dữ liệu. 

#### 1.	Định nghĩa NMF
Cho ma trận **X** gồm **n** dòng, **m** cột. Kỹ thuật NMF sẽ tìm 2 (hoặc 3) ma trận **H**, **W** sao cho, tích **HW** sẽ cho trở lại giá trị xấp xỉ với **X**, nghĩa là, với ma trận **X** được cho trước, tìm **H**, **W** sao cho, $X = HW$

H nxk, W k x m
Lưu ý rằng, k có giá trị rất nhỏ so với n và m. Các ma trận X, H, W đều có ràng buộc không âm, nghĩa là giá trị của các phần tử (element) trong các ma trận này >=0. 


## Themes

Wowchemy and its templates come with **automatic day (light) and night (dark) mode** built-in. Alternatively, visitors can choose their preferred mode - click the moon icon in the top right of the [Demo](https://academic-demo.netlify.com/) to see it in action! Day/night mode can also be disabled by the site admin in `params.toml`.

[Choose a stunning **theme** and **font**](https://wowchemy.com/docs/customization) for your site. Themes are fully customizable.

## License

Copyright 2016-present [George Cushen](https://georgecushen.com).

Released under the [MIT](https://github.com/wowchemy/wowchemy-hugo-modules/blob/master/LICENSE.md) license.

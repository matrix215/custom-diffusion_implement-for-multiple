# Custom diffusion implement for StyleBoost
![1 125599430](https://github.com/matrix215/custom-diffusion_implement-for-StyleBoost/assets/101815603/85879556-5080-44f3-bc9f-ee82cd09fc88)

![0 228097034](https://github.com/matrix215/custom-diffusion_implement-for-StyleBoost/assets/101815603/26c83ac9-1c07-43e8-936a-a7d1615dd5ac)

[Custom Diffusion](https://arxiv.org/abs/2212.04488) is a method to customize text-to-image models like Stable Diffusion given just a few (4~5) images of a subject.
The `train_custom_diffusion.py` script shows how to implement the training procedure and adapt it for stable diffusion.

# Requirements

https://github.com/adobe-research/custom-diffusion

- Go to the custom-diffusion Official page and Follow the preferences

- I did implement at A5000 GPU, But it was a cool environment Because the custom diffusion model is lighter because only the U-Net part is fine-turning during the Stable Diffusion's diffusion process. 

# How to start

### Official pages are not optimized for multiple draws. Therefore, once the weights are stored, a code that draws a large number of them separately based on the prompts in the txt file was created.

- First follow all of custom-diffusion Offical page
- second, ```bash training.ipynb```
- Third, then we can save the weight file
- cmd_multi.py file can start the multiple draws
  - cmd_multi.py can manipulate the number of samples
  - iteration also can manipulate
    ```bash
    python cmd_multi.py --iter 10
    ```

# Acknowledgement
This repository is based on the following repositories:
```bash
@inproceedings{kumari2023multi,
  title={Multi-concept customization of text-to-image diffusion},
  author={Kumari, Nupur and Zhang, Bingliang and Zhang, Richard and Shechtman, Eli and Zhu, Jun-Yan},
  booktitle={Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition},
  pages={1931--1941},
  year={2023}
}
```

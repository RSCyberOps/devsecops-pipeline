![Pipeline Status](https://github.com/RSCyberOps/devsecops-pipeline/actions/workflows/pipeline.yml/badge.svg)

# Projeto DevSecOps Pipeline# Projeto DevSecOps Pipeline

Este projeto é uma API simples em Python (Flask) que utiliza um pipeline de CI/CD no GitHub Actions com um "Security Gate" integrado.

## Ferramentas utilizadas:
* Python e Flask
* Docker
* GitHub Actions
* Trivy (Scanner de vulnerabilidades)

## Como funciona:
A cada `push` na branch `main`, o GitHub Actions constrói a imagem Docker e roda o Trivy. Se forem encontradas vulnerabilidades do tipo CRITICAL ou HIGH, o pipeline falha e o código não avança.

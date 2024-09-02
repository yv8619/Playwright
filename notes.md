## why do we need nodejs for playwright ?
Playwright is built using JavaScript/TypeScript and designed to run in the Node.js environment. Node.js provides the runtime needed to execute JavaScript code on the server side, which is essential for running Playwright scripts.

## what is chocolatey ?
Chocolatey is a package manager for Windows that simplifies the installation, configuration, and management of software similarly to apt for Linux distributions or brew for macOS. Chocolatey provides a command-line interface to install, update, and manage software packages.

Installation: npm init playwright@latest

## what is playwright.config ?
The playwright.config is where you can add configuration for Playwright including modifying which browsers you would like to run Playwright on. If you are running tests inside an already existing project then dependencies will be added directly to your package.json.

import { test, expect } from '@playwright/test';

test('has title', async ({ page }) => {
  await page.goto("https://playwright.dev");
  await expect(page).toHaveTitle("Playwright");
});

## playwright.config.ts
This file will have the info about test to be run, browsers and other configurations. 
npx playwright test

## locators

test('has title', async ({ page }) => {
  await page.goto("https://playwright.dev");
  await expect(page).toHaveTitle("Playwright");
  await page.locator('#username').fill('yash8619');
  await page.locator('#submit').click();
});






